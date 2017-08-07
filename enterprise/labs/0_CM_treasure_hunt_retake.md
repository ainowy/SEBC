<p>
<b>What is ubertask optimization?</b>

When Ubertask optimization is enabled through the parameter "mapreduce.job.ubertask.enable" that is configured in YARN service, 
it allows us to execute the tasks with few map or reduce tasks in only one node. 

MR commands applied to ubertask are: mapreduce.job.ubertask.maxmaps, mapreduce.job.ubertask.maxreduces, and mapreduce.job.ubertask.maxbytes settings.

For further information:

https://archive.cloudera.com/cdh5/cdh/5/hadoop/hadoop-mapreduce-client/hadoop-mapreduce-client-core/mapred-default.xml

<b>Where in CM is the Kerberos Security Realm value displayed?</b>

CM > Click on the search box and type "kerberos security realm"; after that, click on "configuration: security realm" where 
you can find out the property "default_realm".

<b>Which CDH service(s) host a property for enabling Kerberos authentication?</b>

CDH service > Configuration > Type in the search box "Kerberos"
Hadoop Secure Authentication
hadoop.security.authentication: and set this property to Kerberos

<b>How do you upgrade the CM agents?</b>

There are two ways to upgrade CM agents: manual or using CM. I will explain the command way

<b>Give the tsquery statement used to chart Hue's CPU utilization?</b>

select cpu_user_rate where roleType=hue_server

<b>Name all the roles that make up the Hive service</b>

HiveMetastore
HiveServer2
Hive Gateway
WebHcat

<b>What steps must be completed before integrating Cloudera Manager with Kerberos?</b>

Before launching CM's kerberos wizard we should install:

kerberos-server, kerberos-workstation, kerberos-auth-libs in the KDC node 
kerberos-workstation, kerberos-auth-libs in the Kerberos client nodes

Modify the kerberos files in the server node:

-vi /var/kerberos/krb5kdc/kdc.conf 
- vi /var/kerberos/kadmin.acl 
- vi /etc/krb5.conf

Create kerberos database in the KDC node and perform the following steps in the KDC server node:

Start krbkdc service 
Start kadmin service 
chkconfig krbkdc on
chkconfig kadmin on

Once everything has been started properly, we can access from the kdc server node to the kadmin.local console:

#kadmin.local -> here we should add the principals we consider necessary. A must is to add the cloudera-scm principal which should have 
privileges to create other principals (this is specified in the kadmin.acl file)

After following these steps, we can go to CM and launch the Kerberos Wizard

</p>
