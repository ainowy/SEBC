
<b>Check vm.swappiness on all your nodes and set to 1 if necessary</b>
<p>
export NODES="ip-172-31-32-121 ip-172-31-33-23 ip-172-31-32-86 ip-172-31-36-207 ip-172-31-38-126"

[root@ip-172-31-36-207 ~]# for i in `echo $NODES`; do ssh -i  ainhoa_ireland.pem $i echo "vm.swappiness = 1" >> /etc/sysctl.conf; done

<b>Show the mount attributes of your volume(s)</b>

[root@ip-172-31-36-207 ~]# for i in `echo $NODES`; do ssh -i  ainhoa_ireland.pem $i cat /etc/fstab; done
LABEL=centos_root               /        ext4      defaults         0 0
devpts     /dev/pts  devpts  gid=5,mode=620   0 0
tmpfs      /dev/shm  tmpfs   defaults         0 0
proc       /proc     proc    defaults         0 0
sysfs      /sys      sysfs   defaults         0 0
LABEL=centos_root               /        ext4      defaults         0 0
devpts     /dev/pts  devpts  gid=5,mode=620   0 0
tmpfs      /dev/shm  tmpfs   defaults         0 0
proc       /proc     proc    defaults         0 0
sysfs      /sys      sysfs   defaults         0 0
LABEL=centos_root               /        ext4      defaults         0 0
devpts     /dev/pts  devpts  gid=5,mode=620   0 0
tmpfs      /dev/shm  tmpfs   defaults         0 0
proc       /proc     proc    defaults         0 0
sysfs      /sys      sysfs   defaults         0 0
LABEL=centos_root               /        ext4      defaults         0 0
devpts     /dev/pts  devpts  gid=5,mode=620   0 0
tmpfs      /dev/shm  tmpfs   defaults         0 0
proc       /proc     proc    defaults         0 0
sysfs      /sys      sysfs   defaults         0 0
LABEL=centos_root               /        ext4      defaults         0 0
devpts     /dev/pts  devpts  gid=5,mode=620   0 0
tmpfs      /dev/shm  tmpfs   defaults         0 0
proc       /proc     proc    defaults         0 0
sysfs      /sys      sysfs   defaults         0 0

<b>#show the reserve space of any non-root, ext-based volumes</b>

[root@ip-172-31-36-207 ~]# fdisk -l

Disk /dev/xvde: 53.7 GB, 53687091200 bytes
255 heads, 63 sectors/track, 6527 cylinders
Units = cylinders of 16065 * 512 = 8225280 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes
Disk identifier: 0x00000000


[root@ip-172-31-36-207 ~]# for i in  `echo $NODES`; do ssh -i ainhoa_ireland.pem $i df -H ; done
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        53G  690M   50G   2% /
tmpfs           7.9G     0  7.9G   0% /dev/shm
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        53G  690M   50G   2% /
tmpfs           7.9G     0  7.9G   0% /dev/shm
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        53G  690M   50G   2% /
tmpfs           7.9G     0  7.9G   0% /dev/shm
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        53G  690M   50G   2% /
tmpfs           7.9G     0  7.9G   0% /dev/shm
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        53G  690M   50G   2% /
tmpfs           7.9G     0  7.9G   0% /dev/shm

<b>#disable transparent hugepage support:</b>

echo "if test -f /sys/kernel/mm/transparent_hugepage/enabled; then
   echo never > /sys/kernel/mm/transparent_hugepage/enabled
fi
if test -f /sys/kernel/mm/transparent_hugepage/defrag; then
   echo never > /sys/kernel/mm/transparent_hugepage/defrag
fi" >>  /etc/rc.d/rc.local

<b>List your network interface configuration</b>

[root@ip-172-31-36-207 ~]# ifconfig
eth0      Link encap:Ethernet  HWaddr 0A:6C:2A:60:98:18
          inet addr:172.31.36.207  Bcast:172.31.47.255  Mask:255.255.240.0
          inet6 addr: fe80::86c:2aff:fe60:9818/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:1562 errors:0 dropped:0 overruns:0 frame:0
          TX packets:1435 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:205469 (200.6 KiB)  TX bytes:222928 (217.7 KiB)
          Interrupt:24

lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
          inet6 addr: ::1/128 Scope:Host
          UP LOOPBACK RUNNING  MTU:16436  Metric:1
          RX packets:286 errors:0 dropped:0 overruns:0 frame:0
          TX packets:286 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0
          RX bytes:51974 (50.7 KiB)  TX bytes:51974 (50.7 KiB)

<b>Show that forward and reverse host lookups are correctly resolved</b>

For this step, we install bind-utils

[root@ip-172-31-36-207 ~]# nslookup ip-172-31-36-207
Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
Name:   ip-172-31-36-207.eu-west-1.compute.internal
Address: 172.31.36.207

[root@ip-172-31-36-207 ~]# getent hosts 127.0.0.1
127.0.0.1       localhost.localdomain localhost

<b>Show the nscd service is running</b>

[root@ip-172-31-36-207 ~]# for i in `echo $NODES`; do ssh -i ainhoa_ireland.pem $i chkconfig nscd on; ssh -i ainhoa_ireland.pem $i service nscd status; done
nscd (pid 819) is running...
nscd (pid 822) is running...
nscd (pid 820) is running...
nscd (pid 819) is running...
nscd (pid 820) is running...


<b>Show the ntpd service is running</b>

[root@ip-172-31-36-207 ~]# for i in `echo $NODES`; do ssh -i ainhoa_ireland.pem $i chkconfig ntpd on; ssh -i ainhoa_ireland.pem $i service ntpd status; done
ntpd (pid  849) is running...
ntpd (pid  852) is running...
ntpd (pid  850) is running...
ntpd (pid  849) is running...
ntpd (pid  850) is running...




</p>
