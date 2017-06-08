<pre>
<b>[root@ip-172-31-47-133 ~]# curl -u ainowy:cloudera 'http://34.249.47.205:7180/ai/v12/clusters/ainowy/services/hive/'</b>
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-172-31-47-133.eu-west-1.compute.internal:7180/cmf/serviceRedirect/hive",
  "roleInstancesUrl" : "http://ip-172-31-47-133.eu-west-1.compute.internal:7180/cmf/serviceRedirect/hive/instances",
  "serviceState" : "STARTED",
  "healthSummary" : "GOOD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  } ],
  "configStalenessStatus" : "FRESH",
  "clientConfigStalenessStatus" : "FRESH",
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive",
  "entityStatus" : "GOOD_HEALTH"
}[root@ip-172-31-47-133 ~]# clear

<b>[root@ip-172-31-47-133 ~]# curl -u ainowy:cloudera 'http://34.249.47.205:7180/api/v12/clusters/ainowy/services/hive/'</b>
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-172-31-47-133.eu-west-1.compute.internal:7180/cmf/serviceRedirect/hive",
  "roleInstancesUrl" : "http://ip-172-31-47-133.eu-west-1.compute.internal:7180/cmf/serviceRedirect/hive/instances",
  "serviceState" : "STARTED",
  "healthSummary" : "GOOD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  } ],
  "configStalenessStatus" : "FRESH",
  "clientConfigStalenessStatus" : "FRESH",
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive",
  "entityStatus" : "GOOD_HEALTH"

</pre>

<pre>

<b>[root@ip-172-31-47-133 ~]# curl -X POST -u ainowy:cloudera 'http://34.249.47.20:7180/api/v12/clusters/ainowy/services/hive/commands/stop' </b>
{
  "id" : 375,
  "name" : "Stop",
  "startTime" : "2017-06-07T14:50:05.736Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
</pre>
<pre>
<b>[root@ip-172-31-47-133 ~]# curl -X POST -u ainowy:cloudera 'http://34.249.47.205:7180/api/v12/clusters/ainowy/services/hive/commands/start'</b>
{
  "id" : 379,
  "name" : "Start",
  "startTime" : "2017-06-07T14:50:58.342Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
</pre>

