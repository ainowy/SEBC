
<pre>

<b>List the command and output for ls /etc/yum.repos.d</b>

[root@ip-172-31-27-23 ~]# ls /etc/yum.repos.d/
CentOS-Base.repo       CentOS-Vault.repo      mysql-community-source.repo
CentOS-Debuginfo.repo  cloudera-manager.repo
CentOS-Media.repo      mysql-community.repo

<b>Use the scm_prepare_database.sh script to create the db.properties file</b>

[root@ip-172-31-27-23 ~]# /usr/share/cmf/schema/scm_prepare_database.sh -h ip-172-31-21-134 --scm-host ip-172-31-27-23 mysql scm scm T3mp0r@l
JAVA_HOME=/usr/java/jdk1.8.0_91
Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.8.0_91/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
log4j:ERROR Could not find value for key log4j.appender.A
log4j:ERROR Could not instantiate appender named "A".
[2017-08-11 07:21:16,984] INFO     0[main] - com.cloudera.enterprise.dbutil.DbCommandExecutor.testDbConnection(DbCommandExecutor.java) - Successfully connected to database.
<b>All done, your SCM database is configured correctly!</b>


</pre>
