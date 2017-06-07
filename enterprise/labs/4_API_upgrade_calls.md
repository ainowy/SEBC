
<pre>
<h1><b>Check API version</b></h1>
[root@ip-172-31-47-133 ~]# curl -u ainowy:cloudera 'http://34.249.47.205:7180/api/version'
v14

<h1><b>Check CM versionn</b></h1>

[root@ip-172-31-47-133 ~]# curl -u ainowy:cloudera 'http://34.249.47.205:7180/ai/v14/cm/version'
{
  "version" : "5.9.2",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20170330-1814",
  "gitHash" : "822da28bff818f57fc1bfc3eafe3a550300ef1b0",
  "snapshot" : false

<h1><b>List CM users</b></h1>

[root@ip-172-31-47-133 ~]# curl -u ainowy:cloudera 'http://34.249.47.205:7180/ai/v14/users'
{
  "items" : [ {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ]
  }, {
    "name" : "ainowy",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ]
  } ]
  
  
<h1><b>Check MYSQL version</b></h1>
  
[root@ip-172-31-47-133 ~]# curl -u ainowy:cloudera 'http://34.249.47.205:7180/api/v14/cm/scmDbInfo'
{
  "scmDbType" : "MYSQL",
  "embeddedDbUsed" : false
</pre>
