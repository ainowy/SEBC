<pre>
<b>#Check vm.swapiness on all your nodes:</b>

sudo vi /etc/sysctl.conf and we add the line: vm.swappiness = 1 -> we need to reboot the machine

[root@ip-172-31-47-133 ~]# cat /proc/sys/vm/swappiness
1
<b>#show mount attributes of volumes:</b>

[root@ip-172-31-47-133 ~]# cat /etc/fstab
LABEL=centos_root               /        ext4      defaults         0 0
devpts     /dev/pts  devpts  gid=5,mode=620   0 0
tmpfs      /dev/shm  tmpfs   defaults         0 0
proc       /proc     proc    defaults         0 0
sysfs      /sys      sysfs   defaults         0 0

[root@ip-172-31-47-133 ~]# lsblk
NAME MAJ:MIN RM SIZE RO TYPE MOUNTPOINT
xvde 202:64   0  30G  0 disk /

<b>#show the reserve space of any non-root, ext-based volumes:</b>

we first check the name of our disk(s):
[root@ip-172-31-47-133 ~]# fdisk -l

Disk /dev/xvde: 32.2 GB, 32212254720 bytes
255 heads, 63 sectors/track, 3916 cylinders
Units = cylinders of 16065 * 512 = 8225280 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes
Disk identifier: 0x00000000



<b>#disable transparent hugepage support:</b>

I do not have transparent_hugepages enabled in my kernel by default

<b>#list the network interface configuration:</b>

root@ip-172-31-47-133 ~]# ifconfig

eth0      Link encap:Ethernet  HWaddr 0A:DE:B6:9D:BC:22
          inet addr:172.31.47.133  Bcast:172.31.47.255  Mask:255.255.240.0
          inet6 addr: fe80::8de:b6ff:fe9d:bc22/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:1994523 errors:0 dropped:0 overruns:0 frame:0
          TX packets:1608811 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:2637192365 (2.4 GiB)  TX bytes:3361018546 (3.1 GiB)
          Interrupt:24

lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
          inet6 addr: ::1/128 Scope:Host
          UP LOOPBACK RUNNING  MTU:16436  Metric:1
          RX packets:592798 errors:0 dropped:0 overruns:0 frame:0
          TX packets:592798 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0
          RX bytes:2051188652 (1.9 GiB)  TX bytes:2051188652 (1.9 GiB)



<b>#list forward and reverse host lookups:</b>
 as nslokup is not installed. First we need to install bind-utils

[root@ip-172-31-47-133 ~]# nslookup ip-172-31-47-133
Server:         172.31.0.2
Address:        172.31.0.2#53

<b>#status nscd:</b>

[root@ip-172-31-47-133 ~]# service nscd status
nscd (pid 1043) is running...
