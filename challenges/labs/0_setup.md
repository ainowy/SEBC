<pre>

<b>List the cloud provider you are using (AWS, GCE, Azure, other)</b>

My Cloud Provider: AWS

<b>List the Linux release you have chosen:</b>

[root@ip-172-31-41-46 ~]# cat /etc/redhat-release
CentOS release 6.5 (Final)


<b>Show that the disk space on each node is at least 30 GB</b>

[root@ip-172-31-41-46 ~]# export NODES="ip-172-31-41-46 ip-172-31-36-216  ip-172-31-39-38 ip-172-31-40-250 ip-172-31-36-114"


[root@ip-172-31-41-46 ~]# for i in  `echo $NODES`; do ssh -i Cluster.pem $i df -H ; done
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde       106G  809M  100G   1% /
tmpfs           7.9G     0  7.9G   0% /dev/shm
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        32G  6.8G   24G  23% /
tmpfs           7.9G     0  7.9G   0% /dev/shm
cm_processes    7.9G  5.5M  7.9G   1% /var/run/cloudera-scm-agent/process
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde       106G  704M  100G   1% /
tmpfs           7.9G     0  7.9G   0% /dev/shm
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde       106G  714M  100G   1% /
tmpfs           7.9G     0  7.9G   0% /dev/shm
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde       106G  708M  100G   1% /
tmpfs           7.9G     0  7.9G   0% /dev/sh

<b>List the command and output for yum repolist enabled</b>

[root@ip-172-31-41-46 ~]#  for i in  `echo $NODES`; do ssh -i Cluster.pem $i yum repolist enabled; done
Loaded plugins: fastestmirror, presto
Loading mirror speeds from cached hostfile
 * base: ftp.heanet.ie
 * extras: ftp.heanet.ie
 * updates: ftp.heanet.ie
repo id                        repo name                                  status
base                           CentOS-6 - Base                            6,706
extras                         CentOS-6 - Extras                             45
updates                        CentOS-6 - Updates                           354
repolist: 7,105
Loaded plugins: fastestmirror, presto
Loading mirror speeds from cached hostfile
 * base: ftp.heanet.ie
 * extras: ftp.heanet.ie
 * updates: ftp.heanet.ie
repo id                           repo name                               status
base                              CentOS-6 - Base                         6,706
cloudera-manager                  Cloudera Manager, Version 5.9.2             7
extras                            CentOS-6 - Extras                          45
mysql-connectors-community        MySQL Connectors Community                 36
mysql-tools-community             MySQL Tools Community                      47
mysql57-community                 MySQL 5.7 Community Server                183
updates                           CentOS-6 - Updates                        354
repolist: 7,378
Loaded plugins: fastestmirror, presto
repo id                        repo name                                  status
base                           CentOS-6 - Base                            6,706
extras                         CentOS-6 - Extras                             45
updates                        CentOS-6 - Updates                           354
repolist: 7,105
Loaded plugins: fastestmirror, presto
repo id                        repo name                                  status
base                           CentOS-6 - Base                            6,706
extras                         CentOS-6 - Extras                             45
updates                        CentOS-6 - Updates                           354
repolist: 7,105
Loaded plugins: fastestmirror, presto
repo id                        repo name                                  status
base                           CentOS-6 - Base                            6,706
extras                         CentOS-6 - Extras                             45
updates                        CentOS-6 - Updates                           354
repolist: 7,105

<b>Add the following Linux accounts to all nodes</b>

[root@ip-172-31-41-46 ~]# export NODES="ip-172-31-41-46 ip-172-31-36-216  ip-172-31-39-38 ip-172-31-40-250 ip-172-31-36-114"
[root@ip-172-31-41-46 ~]#  for i in  `echo $NODES`; do ssh -i Cluster.pem $i egrep "jeremy" /etc/passwd; done
jeremy:x:3000:3000::/home/jeremy:/bin/bash
jeremy:x:3000:3000::/home/jeremy:/bin/bash
jeremy:x:3000:3000::/home/jeremy:/bin/bash
jeremy:x:3000:3000::/home/jeremy:/bin/bash
jeremy:x:3000:3000::/home/jeremy:/bin/bash

[root@ip-172-31-41-46 ~]#  for i in  `echo $NODES`; do ssh -i Cluster.pem $i egrep "theresa" /etc/passwd; done
theresa:x:2000:2000::/home/theresa:/bin/bash
theresa:x:2000:2000::/home/theresa:/bin/bash
theresa:x:2000:2000::/home/theresa:/bin/bash
theresa:x:2000:2000::/home/theresa:/bin/bash
theresa:x:2000:2000::/home/theresa:/bin/bash

[root@ip-172-31-41-46 ~]#  for i in  `echo $NODES`; do ssh -i Cluster.pem $i egrep "labour" /etc/group; done
labour:x:3002:jeremy
labour:x:3002:jeremy
labour:x:3002:jeremy
labour:x:3002:jeremy
labour:x:3002:jeremy

[root@ip-172-31-41-46 ~]#  for i in  `echo $NODES`; do ssh -i Cluster.pem $i egrep "conservative" /etc/group; done
conservative:x:3001:theresa
conservative:x:3001:theresa
conservative:x:3001:theresa
conservative:x:3001:theresa
conservative:x:3001:theresa

</pre>
