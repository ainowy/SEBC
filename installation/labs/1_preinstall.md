#My cluster is formed by(see 0_nodes.md) -> in order to work better with the machines, the /etc/hosts of each machine has been modified:
<br>
172.31.45.11 cloudera
<br>
172.31.42.71 master
<br>
172.31.38.231 worker1
<br>
172.31.41.56 worker2
<br>
172.31.47.219 worker3
<br>

#Check vm.swapiness on all your nodes:

cat /proc/sys/vm/swapiness

[centos@ip-172-31-45-11 ~]$ sudo cat /proc/sys/vm/swappiness
30

#Set swappiness to = 1:

sudo vi /etc/sysctl.conf and we add the line: vm.swappiness = 1 -> we need to reboot the machine

command line: sudo sysctl vm.swappiness=1
<br>
[centos@ip-172-31-45-11 ~]$ sudo sysctl vm.swappiness=1
vm.swappiness = 1
<br>
[centos@ip-172-31-42-71 ~]$ sudo cat /proc/sys/vm/swappiness
1
<br>
[centos@ip-172-31-38-231 ~]$ sudo sysctl vm.swappiness=1
vm.swappiness = 1
<br>
[centos@ip-172-31-41-56 ~]$ sudo sysctl vm.swappiness=1
vm.swappiness = 1
<br>
[centos@worker3 ~]$ sudo sysctl vm.swappiness=1
vm.swappiness = 1
<br>
#show mount attributes of volumes:

[root@master transparent_hugepage]# cat /etc/fstab

#
# /etc/fstab
# Created by anaconda on Mon May  1 18:59:01 2017
#
# Accessible filesystems, by reference, are maintained under '/dev/disk'
# See man pages fstab(5), findfs(8), mount(8) and/or blkid(8) for more info
#
UUID=29342a0b-e20f-4676-9ecf-dfdf02ef6683 /                       xfs     defaul                                                                                        ts        0 0
<br>
[root@master ~]# lsblk
NAME    MAJ:MIN RM SIZE RO TYPE MOUNTPOINT
xvda    202:0    0  30G  0 disk
└─xvda1 202:1    0  30G  0 part /

[root@master ~]# fdisk -l
<br>
Disk /dev/xvda: 32.2 GB, 32212254720 bytes, 62914560 sectors
<br>
Units = sectors of 1 * 512 = 512 bytes
<br>
Sector size (logical/physical): 512 bytes / 512 bytes
<br>
I/O size (minimum/optimal): 512 bytes / 512 bytes
<br>
Disk label type: dos
<br>
Disk identifier: 0x000b2270

    Device Boot      Start         End      Blocks   Id  System
/dev/xvda1   *        2048    62910539    31454246   83  Linux


#show the reserve space of any non-root, ext-based volumes:

I'm not using any ext-based volume

#disable transparent hugepage support:

to check status: /sys/kernel/mm/transparent_hugepage/enabled
<br>
[root@master transparent_hugepage]# echo never > /sys/kernel/mm/transparent_hugepage/enabled
<br>
[root@master transparent_hugepage]# cat /sys/kernel/mm/transparent_hugepage/enabled
always madvise [never]
<br>
#list the network interface configuration:
<br>
[centos@master transparent_hugepage]$ ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001
        inet 172.31.42.71  netmask 255.255.240.0  broadcast 172.31.47.255
        inet6 fe80::80d:dcff:fea0:1e7  prefixlen 64  scopeid 0x20<link>
        ether 0a:0d:dc:a0:01:e7  txqueuelen 1000  (Ethernet)
        RX packets 23800  bytes 31442819 (29.9 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 11498  bytes 932487 (910.6 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1  (Local Loopback)
        RX packets 6  bytes 416 (416.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 6  bytes 416 (416.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
<br>
#list forward and reverse host lookups:
 as nslokup is not installed. First we need to install bind-utils

[centos@master transparent_hugepage]$ nslookup master
Server:         172.31.0.2
Address:        172.31.0.2#53

<br>
#show nscd/ntpd service is running:

as none of the services were installed on CentOs I'm using, we have to install 
both commands:
<br>
[centos@master ~]$ sudo yum install -y ntp nscd
<br>
[centos@master ~]$ sudo chkconfig ntpd on
Note: Forwarding request to 'systemctl enable ntpd.service'.
Created symlink from /etc/systemd/system/multi-user.target.wants/ntpd.service to /usr/lib/systemd/system/ntpd.service.
<br>
[centos@master ~]$ sudo service ntpd start
Redirecting to /bin/systemctl start  ntpd.service
<br>
[centos@master ~]$ sudo chkconfig nscd on
Note: Forwarding request to 'systemctl enable nscd.service'.
Created symlink from /etc/systemd/system/multi-user.target.wants/nscd.service to /usr/lib/systemd/system/nscd.service.
Created symlink from /etc/systemd/system/sockets.target.wants/nscd.socket to /usr/lib/systemd/system/nscd.socket.
<br>
[centos@master ~]$ sudo service nscd start
Redirecting to /bin/systemctl start  nscd.service
<br>
[centos@master ~]$ sudo service ntpd start
Redirecting to /bin/systemctl start  ntpd.service
<br>
[centos@master ~]$ sudo service nscd status
Redirecting to /bin/systemctl status  nscd.service
● nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; enabled; vendor preset: disabled)
   Active: active (running) since Mon 2017-06-05 14:11:53 UTC; 27s ago
  Process: 16695 ExecStart=/usr/sbin/nscd $NSCD_OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 16696 (nscd)
   CGroup: /system.slice/nscd.service
           └─16696 /usr/sbin/nscd
<br>
Jun 05 14:11:53 master nscd[16696]: 16696 monitoring directory `/etc` (2)
<br>
Jun 05 14:11:53 master nscd[16696]: 16696 monitoring file `/etc/resolv.conf` (5)
<br>
Jun 05 14:11:53 master nscd[16696]: 16696 monitoring directory `/etc` (2)
<br>
Jun 05 14:11:53 master nscd[16696]: 16696 monitoring file `/etc/services` (6)
<br>
Jun 05 14:11:53 master nscd[16696]: 16696 monitoring directory `/etc` (2)
<br>
Jun 05 14:11:53 master nscd[16696]: 16696 disabled inotify-based monitoring...ry
<br>
Jun 05 14:11:53 master nscd[16696]: 16696 stat failed for file `/etc/netgro...ry
Jun 05 14:11:53 master nscd[16696]: 16696 Access Vector Cache (AVC) started
Jun 05 14:11:53 master systemd[1]: Started Name Service Cache Daemon.
Jun 05 14:12:12 master nscd[16696]: 16696 checking for monitored file `/etc...ry
Hint: Some lines were ellipsized, use -l to show in full.

