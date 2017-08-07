<h1><b> Setup your cluster </b></h1>

<p>
<b>List the cloud provider you are using (AWS, GCE, Azure, CloudCat, other)</b>

My Cloud Provider is AWS

<b>List your instances by IP address and DNS name (don't use /etc/hosts for this)</b>

54.171.99.171 ec2-54-171-99-171.eu-west-1.compute.amazonaws.com
34.253.231.120 ec2-34-253-231-120.eu-west-1.compute.amazonaws.com
54.194.23.52 ec2-54-194-23-52.eu-west-1.compute.amazonaws.com
54.229.129.4 ec2-54-229-129-4.eu-west-1.compute.amazonaws.com
54.246.252.188 ec2-54-246-252-188.eu-west-1.compute.amazonaws.com

<b>List the Linux release you are using</b>

[root@ip-172-31-12-138 ~]# cat /etc/redhat-release
CentOS release 6.5 (Final)

<b>List the command and output for yum repolist enabled</b>

[root@ip-172-31-12-138 ~]# yum repolist enabled
Loaded plugins: fastestmirror, presto
Loading mirror speeds from cached hostfile
 * base: ftp.heanet.ie
 * extras: ftp.heanet.ie
 * updates: ftp.heanet.ie
repo id                                repo name                                    status
base                                   CentOS-6 - Base                              6,706
extras                                 CentOS-6 - Extras                               45
updates                                CentOS-6 - Updates                             447
repolist: 7,198

<b>Add the following Linux accounts to all nodes</b>

User saturn with a UID of 2800
User haley with a UID of 2900
Create the group comets and add haley to it
Create the group planets and add saturn to it

for i in `echo $NODES`; do ssh -i ainhoa_ireland.pem $i useradd -u 2801  saturn; done
for i in `echo $NODES`; do ssh -i ainhoa_ireland.pem $i useradd -u 2901 haley; done

for i in `echo $NODES`; do ssh -i ainhoa_ireland.pem $i groupadd comets; done
for i in `echo $NODES`; do ssh -i ainhoa_ireland.pem $i groupadd planets; done

for i in `echo $NODES`; do ssh -i ainhoa_ireland.pem $i usermod -a -G comets haley; done
for i in `echo $NODES`; do ssh -i ainhoa_ireland.pem $i usermod -a -G planets saturn; done

<b>List the /etc/passwd entries for saturn and haley</b>

[root@ip-172-31-12-138 ~]# for i in `echo $NODES`; do ssh -i ainhoa_ireland.pem $i cat /etc/passwd | grep "haley"; done
haley:x:2901:2901::/home/haley:/bin/bash
haley:x:2901:2901::/home/haley:/bin/bash
haley:x:2901:2901::/home/haley:/bin/bash
haley:x:2901:2901::/home/haley:/bin/bash
haley:x:2901:2901::/home/haley:/bin/bash

[root@ip-172-31-12-138 ~]# for i in `echo $NODES`; do ssh -i ainhoa_ireland.pem $i cat /etc/passwd | grep "saturn"; done
saturn:x:2801:2803::/home/saturn:/bin/bash
saturn:x:2801:2803::/home/saturn:/bin/bash
saturn:x:2801:2803::/home/saturn:/bin/bash
saturn:x:2801:2803::/home/saturn:/bin/bash
saturn:x:2801:2803::/home/saturn:/bin/bash

<b>List the /etc/group entries for comets and planets</b>
[root@ip-172-31-12-138 ~]# for i in `echo $NODES`; do ssh -i ainhoa_ireland.pem $i cat /etc/group | grep "comets"; done
comets:x:2902:haley
comets:x:2902:haley
comets:x:2902:haley
comets:x:2902:haley
comets:x:2902:haley

[root@ip-172-31-12-138 ~]# for i in `echo $NODES`; do ssh -i ainhoa_ireland.pem $i cat /etc/group | grep "planets"; done
planets:x:2903:saturn
planets:x:2903:saturn
planets:x:2903:saturn
planets:x:2903:saturn
planets:x:2903:saturn

</p>



