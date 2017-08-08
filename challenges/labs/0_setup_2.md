<p>

<b>Region, AWS Id, OS</b>

Region: Ireland
AWS ID:
OS: 
[root@ip-172-31-12-49 ~]# cat /etc/redhat-release
CentOS release 6.5 (Final)

<b> Available disk space on each node </b>
[root@ip-172-31-12-49 ~]# df -H
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        32G  833M   30G   3% /
tmpfs           4.0G     0  4.0G   0% /dev/shm

<b>Following accounts on each node</b>

[root@ip-172-31-12-49 ~]# for i in `echo $NODES`; do ssh -i ainhoa_ireland.pem $i cat /etc/passwd | grep "saxony"; done
saxony:x:2700:500::/home/saxony:/bin/bash
saxony:x:2700:500::/home/saxony:/bin/bash
saxony:x:2700:500::/home/saxony:/bin/bash
saxony:x:2700:500::/home/saxony:/bin/bash
saxony:x:2700:500::/home/saxony:/bin/bash

[root@ip-172-31-12-49 ~]# for i in `echo $NODES`; do ssh -i ainhoa_ireland.pem $i cat /etc/passwd | grep "bavaria"; done
bavaria:x:2800:501::/home/bavaria:/bin/bash
bavaria:x:2800:501::/home/bavaria:/bin/bash
bavaria:x:2800:501::/home/bavaria:/bin/bash
bavaria:x:2800:501::/home/bavaria:/bin/bash
bavaria:x:2800:501::/home/bavaria:/bin/bash

[root@ip-172-31-12-49 ~]# for i in `echo $NODES`; do ssh -i ainhoa_ireland.pem $i cat /etc/group | grep "democratic"; done
democratic:x:500:
democratic:x:500:
democratic:x:500:
democratic:x:500:
democratic:x:500:

[root@ip-172-31-12-49 ~]# for i in `echo $NODES`; do ssh -i ainhoa_ireland.pem $i cat /etc/group | grep "social"; done
social:x:501:
social:x:501:
social:x:501:
social:x:501:
social:x:501:


</p>


