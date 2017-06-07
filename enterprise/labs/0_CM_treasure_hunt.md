<pre>

<b>What is ubertask optimization?</b>

When Ubertask optimization is enabled through the parameter "mapreduce.job.ubertask.enable" that is configured in YARN service, 
it allows us to execute the tasks with few map or reduce tasks in only one node. 

MR commands applied to ubertask are: mapreduce.job.ubertask.maxmaps, mapreduce.job.ubertask.maxreduces, and mapreduce.job.ubertask.maxbytes settings.

For further information:

https://archive.cloudera.com/cdh5/cdh/5/hadoop/hadoop-mapreduce-client/hadoop-mapreduce-client-core/mapred-default.xml

<b/Where in CM is the Kerberos Security Realm value displayed?</b>

CM > Click on the search box and type "kerberos security realm"; after that, click on "configuration: security realm" where 
you can find out the property "default_realm".

<b>Which CDH service(s) host a property for enabling Kerberos authentication?</b>

We can enable kerberos authentication in different levels:

-Enable in Zookeeper
-Enable in Yarn, HDFS
-Webconsoles (HTTP)

Besides, there are also other services in which we can enable Kerberos. However, in order to answer this question, I will take into 
account only the ones which have been installed in the cluster for this course.

<b>How do you upgrade the CM agents?</b>

There are two ways to upgrade CM agents: manual or using CM. I will explain the command way

The following commands are for CentOs 6

Stop agent: service cloudera-scm-agent stop
upgrade packets: yum upgrade cloudera-manager-agent
start agent: sudo service cloudera-scm-agent start

<b>Give the tsquery statement used to chart Hue's CPU utilization?</b>

select cpu_user_rate where roleType=hue_server

<b>Name all the roles that make up the Hive service</b>

HiveMetastore
HiveServer2
Hive Gateway
WebHcat

<b>What steps must be completed before integrating Cloudera Manager with Kerberos?</b>

Before completing CM with kerberos you have to install krb5-workstation and auth-libs in all nodes and krb5-server in the KDC node. Also, 
in this file we should specify the type of encryption that our tickets will have.
Besides, we have to setup the kdc.conf file and kadmin.acl. In the kdc.conf we will have to specify which will be our KDC server and 
For this reason, as Cloudera needs an admin principal that allows it to create automatically the principals for the services, 
we will have to create a CM principal so that it can do so. The other configuration file that we should modify if we were not using CM is
krb5.conf. However, the best to do is to allow CM to manage the file as it will modify it according to the configuration that we 
establish through the wizard and distribute it to the rest of the nodes. A bboring and heavy task we can avoid by using CM.

These steps will be reminded in Cloudera before starting the wizard.

</pre>
