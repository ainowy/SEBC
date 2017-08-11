<pre>

<b>List the cloud provider you are using (AWS, GCE, Azure, CloudCat, other)</b>

Cloud Provider: AWS

<b>List your instances by IP address and DNS name (don't use /etc/hosts for this)</b>

54.171.238.114 ip-172-31-21-134.eu-west-1.compute.internal ec2-54-171-238-114.eu-west-1.compute.amazonaws.com
34.253.183.12 ip-172-31-27-23.eu-west-1.compute.internal ec2-34-253-183-12.eu-west-1.compute.amazonaws.com
54.194.124.47 ip-172-31-23-11.eu-west-1.compute.internal ec2-54-194-124-47.eu-west-1.compute.amazonaws.com
54.246.158.204 ip-172-31-19-53.eu-west-1.compute.internal ec2-54-246-158-204.eu-west-1.compute.amazonaws.com
176.34.121.87 ip-172-31-27-203.eu-west-1.compute.internal ec2-176-34-121-87.eu-west-1.compute.amazonaws.com

<b>List the Linux release you are using</b>

[root@ip-172-31-21-134 ~]# cat /etc/redhat-release
CentOS release 6.5 (Final)

<b>List the file system capacity for the first node</b>

[root@ip-172-31-21-134 ~]# df -H

Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde       106G  740M  100G   1% /
tmpfs           7.9G     0  7.9G   0% /dev/shm

<b>List the command and output for yum repolist enabled</b>
[root@ip-172-31-21-134 ~]# yum repolist enabled
Loaded plugins: fastestmirror, presto
Determining fastest mirrors
 * base: repo.uk.bigstepcloud.com
 * extras: mirror.vorboss.net
 * updates: centos.serverspace.co.uk
base                                                     | 3.7 kB     00:00
extras                                                   | 3.4 kB     00:00
updates                                                  | 3.4 kB     00:00
repo id                        repo name                                  status
base                           CentOS-6 - Base                            6,706
extras                         CentOS-6 - Extras                             45
updates                        CentOS-6 - Updates                           447
repolist: 7,198

<b>List the /etc/passwd entries for nimbus and igneous</b>

[root@ip-172-31-21-134 ~]# for i in `echo $NODES`; do ssh -i ainhoa_ireland.pem $i cat /etc/passwd | grep "igneous"; done
igneous:x:2010:500::/home/igneous:/bin/bash
igneous:x:2010:500::/home/igneous:/bin/bash
igneous:x:2010:500::/home/igneous:/bin/bash
igneous:x:2010:500::/home/igneous:/bin/bash
igneous:x:2010:500::/home/igneous:/bin/bash

[root@ip-172-31-21-134 ~]# for i in `echo $NODES`; do ssh -i ainhoa_ireland.pem $i cat /etc/passwd | grep "nimbus"; done
nimbus:x:2016:501::/home/nimbus:/bin/bash
nimbus:x:2016:501::/home/nimbus:/bin/bash
nimbus:x:2016:501::/home/nimbus:/bin/bash
nimbus:x:2016:501::/home/nimbus:/bin/bash
nimbus:x:2016:501::/home/nimbus:/bin/bash

<b>List the /etc/group entries for rocks and clouds</b>

[root@ip-172-31-21-134 ~]# for i in `echo $NODES`; do ssh -i ainhoa_ireland.pem $i cat /etc/group | grep "rocks"; done
rocks:x:500:
rocks:x:500:
rocks:x:500:
rocks:x:500:
rocks:x:500:

[root@ip-172-31-21-134 ~]# for i in `echo $NODES`; do ssh -i ainhoa_ireland.pem $i cat /etc/group | grep "clouds"; done
clouds:x:501:
clouds:x:501:
clouds:x:501:
clouds:x:501:
clouds:x:501:







</pre>
