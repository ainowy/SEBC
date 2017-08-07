<b>Report the latest available version of the API</b>

[root@ip-172-31-38-126 ~]# curl -u admin:admin 'http://54.154.59.148:7180/apirsion'
v16

<b>Report the CM version</b>

[root@ip-172-31-38-126 ~]# curl -u admin:admin 'http://54.154.59.148:7180/api/v14/cm/version'
{
  "version" : "5.12.0",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20170706-1633",
  "gitHash" : "34cb1d666e5618595de85d00a25a02eac120feb4",
  "snapshot" : false
}
<b>List all CM users</b>

[root@ip-172-31-38-126 ~]# curl -u admin:admin 'http://54.154.59.148:7180/api/v14/users'
{
  "items" : [ {
    "name" : "admin",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ]
  } ]

<b>Report the database server in use by CM</b>

[root@ip-172-31-38-126 ~]# curl -u admin:admin 'http://54.154.59.148:7180/api/v14/cm/scmDbInfo'
{
  "scmDbType" : "MYSQL",
  "embeddedDbUsed" : false
}
