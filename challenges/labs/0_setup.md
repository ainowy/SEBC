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
tmpfs           7.9G     0  7.9G   0% /dev/shm

</pre>
