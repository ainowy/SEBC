<h1>Challenge 3 - Install CDH 5.9</h1>

<b>The command and output for hdfs dfs -ls /user</b>

[root@ip-172-31-12-138 ~]# hdfs dfs -ls /user
Found 9 items
drwxr-xr-x   - admin  admin               0 2017-08-07 08:12 /user/admin
drwxr-xr-x   - haley  supergroup          0 2017-08-07 09:20 /user/haley
drwxr-xr-x   - hdfs   supergroup          0 2017-08-07 08:11 /user/hdfs
drwxrwxrwx   - mapred hadoop              0 2017-08-07 07:38 /user/history
drwxrwxr-t   - hive   hive                0 2017-08-07 07:39 /user/hive
drwxrwxr-x   - hue    hue                 0 2017-08-07 07:40 /user/hue
drwxrwxr-x   - oozie  oozie               0 2017-08-07 07:40 /user/oozie
drwxr-xr-x   - saturn supergroup          0 2017-08-07 08:49 /user/saturn
drwxr-x--x   - spark  spark               0 2017-08-07 08:08 /user/spark

<b>The command and output from the CM API call</b>

<p>
[root@ip-172-31-12-138 ~]# curl -u admin:admin http://34.253.231.120:7180/api/v14/hosts
{
  "items" : [ {
    "hostId" : "i-03f2d2dd900c33710",
    "ipAddress" : "172.31.12.138",
    "hostname" : "ip-172-31-12-138.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-2-138.eu-west-1.compute.internal:7180/cmf/hostRedirect/i-03f2d2dd900c33710",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 2,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 7829299200
  }, {
    "hostId" : "i-02a33121ec71e96be",
    "ipAddress" : "172.31.13.174",
    "hostname" : "ip-172-31-13-174.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-2-138.eu-west-1.compute.internal:7180/cmf/hostRedirect/i-02a33121ec71e96be",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 2,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 7829299200
  }, {
    "hostId" : "i-0444d2369ca0509ba",
    "ipAddress" : "172.31.14.161",
    "hostname" : "ip-172-31-14-161.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-2-138.eu-west-1.compute.internal:7180/cmf/hostRedirect/i-0444d2369ca0509ba",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 2,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 7829299200
  }, {
    "hostId" : "i-0714039a637a21930",
    "ipAddress" : "172.31.2.138",
    "hostname" : "ip-172-31-2-138.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-2-138.eu-west-1.compute.internal:7180/cmf/hostRedirect/i-0714039a637a21930",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 2,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 7829299200
  }, {
    "hostId" : "i-0193acda6c29789bf",
    "ipAddress" : "172.31.7.144",
    "hostname" : "ip-172-31-7-144.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-2-138.eu-west-1.compute.internal:7180/cmf/hostRedirect/i-0193acda6c29789bf",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 2,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 7829299200
  } ]
}
</p>

<p>
<b>The command and output from the CM API call</b>

[root@ip-172-31-12-138 ~]# curl -u admin:admin http://34.253.231.120:7180/api/v8/clustersainowy/services
{
  "items" : [ {
    "name" : "zookeeper",
    "type" : "ZOOKEEPER",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-2-138.eu-west-1.compute.internal:7180/cmf/serviceRedirect/zookeeper",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "ZOOKEEPER_CANARY_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "ZOOKEEPER_SERVERS_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "ZooKeeper"
  }, {
    "name" : "oozie",
    "type" : "OOZIE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-2-138.eu-west-1.compute.internal:7180/cmf/serviceRedirect/oozie",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "OOZIE_OOZIE_SERVERS_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Oozie"
  }, {
    "name" : "hue",
    "type" : "HUE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-2-138.eu-west-1.compute.internal:7180/cmf/serviceRedirect/hue",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HUE_HUE_SERVERS_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "HUE_KT_RENEWERS_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Hue"
  }, {
    "name" : "hdfs",
    "type" : "HDFS",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-2-138.eu-west-1.compute.internal:7180/cmf/serviceRedirect/hdfs",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HDFS_BLOCKS_WITH_CORRUPT_REPLICAS",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_CANARY_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_DATA_NODES_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_FREE_SPACE_REMAINING",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_HA_NAMENODE_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_MISSING_BLOCKS",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_UNDER_REPLICATED_BLOCKS",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "HDFS"
  }, {
    "name" : "yarn",
    "type" : "YARN",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-2-138.eu-west-1.compute.internal:7180/cmf/serviceRedirect/yarn",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "YARN_JOBHISTORY_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "YARN_NODE_MANAGERS_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "YARN_RESOURCEMANAGERS_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "YARN_USAGE_AGGREGATION_HEALTH",
      "summary" : "DISABLED"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "YARN (MR2 Included)"
  }, {
    "name" : "hive",
    "type" : "HIVE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-2-138.eu-west-1.compute.internal:7180/cmf/serviceRedirect/hive",
    "serviceState" : "STARTED",
    "healthSummary" : "CONCERNING",
    "healthChecks" : [ {
      "name" : "HIVE_HIVEMETASTORES_HEALTHY",
      "summary" : "CONCERNING"
    }, {
      "name" : "HIVE_HIVESERVER2S_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Hive"
  }, {
    "name" : "spark_on_yarn",
    "type" : "SPARK_ON_YARN",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-2-138.eu-west-1.compute.internal:7180/cmf/serviceRedirect/spark_on_yarn",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Spark"
  } ]
}
</p>
