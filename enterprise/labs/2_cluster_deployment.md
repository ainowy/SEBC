<pre>


[root@ip-172-31-47-133 ~]# curl -u ainowy:cloudera 'http://34.249.47.205:7180/api/v12/cm/deployment' > cm-deployment.json

[root@ip-172-31-47-133 ~]# cat cm-deployment.json
{
  "timestamp" : "2017-06-07T14:45:53.885Z",
  "clusters" : [ {
    "name" : "cluster",
    "displayName" : "ainowy",
    "version" : "CDH5",
    "fullVersion" : "5.8.3",
    "services" : [ {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-b174f6d748bb2e785de46822c2491c1e",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-0fb0c30f993032b36"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "59kx2za9p1wh9jvv27vi8zh7u"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "zookeeper-SERVER-BASE"
        }
      }, {
        "name" : "zookeeper-SERVER-bd3d7eb41c2bd0bd33632df5f6dd504a",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-0acae7e6fe7ad4f40"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2ujjisspnf03ph4823iq3lc90"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "zookeeper-SERVER-BASE"
        }
      }, {
        "name" : "zookeeper-SERVER-d78e8ec89a6e80b5cdfa18d7fa49b600",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-054e4fabb1c61dd56"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "27ikqtn44buvtu3ml0ph6s3ty"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "zookeeper-SERVER-BASE"
        }
      } ],
      "displayName" : "ZooKeeper",
      "roleConfigGroups" : [ {
        "name" : "zookeeper-SERVER-BASE",
        "displayName" : "Server Default Group",
        "roleType" : "SERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "zookeeper"
        },
        "config" : {
          "items" : [ {
            "name" : "zookeeper_server_java_heapsize",
            "value" : "893386752"
          } ]
        }
      } ]
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "items" : [ {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-d78e8ec89a6e80b5cdfa18d7fa49b600",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "i-054e4fabb1c61dd56"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4dwxj7yaj8xuhm4ogop2q8bk0"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "oozie-OOZIE_SERVER-BASE"
        }
      } ],
      "displayName" : "Oozie",
      "roleConfigGroups" : [ {
        "name" : "oozie-OOZIE_SERVER-BASE",
        "displayName" : "Oozie Server Default Group",
        "roleType" : "OOZIE_SERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "oozie"
        },
        "config" : {
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "ip-172-31-47-133.eu-west-1.compute.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "T3mp0r@l"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie"
          }, {
            "name" : "oozie_java_heapsize",
            "value" : "893386752"
          } ]
        }
      } ]
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-172-31-47-133.eu-west-1.compute.internal"
        }, {
          "name" : "database_password",
          "value" : "T3mp0r@l"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-HTTPFS-d78e8ec89a6e80b5cdfa18d7fa49b600"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-d78e8ec89a6e80b5cdfa18d7fa49b600",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "i-054e4fabb1c61dd56"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bt7s92lafehrg4h8gle7n3lsc"
          }, {
            "name" : "secret_key",
            "value" : "KczzRbalFXbucsVK1lZ9oZ5yGaNupG"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hue-HUE_SERVER-BASE"
        }
      } ],
      "displayName" : "Hue",
      "roleConfigGroups" : [ {
        "name" : "hue-HUE_LOAD_BALANCER-BASE",
        "displayName" : "Load Balancer Default Group",
        "roleType" : "HUE_LOAD_BALANCER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hue"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hue-HUE_SERVER-BASE",
        "displayName" : "Hue Server Default Group",
        "roleType" : "HUE_SERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hue"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hue-KT_RENEWER-BASE",
        "displayName" : "Kerberos Ticket Renewer Default Group",
        "roleType" : "KT_RENEWER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hue"
        },
        "config" : {
          "items" : [ ]
        }
      } ]
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "2Wdc6QF4P4hSeThtGYIMRQyPsbZwNx"
        }, {
          "name" : "dfs_ha_fencing_methods",
          "value" : "shell(true)"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "lS1PQLv6EnkpoYg4yBOxd9fI8h8Nz0"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "5i1Wlw3wuBfgQXqHFeZxB5hMlIY9Mn"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "90"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-42d49814318c11e43c1e4054e616215f",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "i-093a5047b66ade686"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-BALANCER-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-55ada182df2a511076bcf7535a2b966e",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-0be3621b8aef0a06a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6xlptjmqj1p2u88yp9zxgaoys"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-b174f6d748bb2e785de46822c2491c1e",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-0fb0c30f993032b36"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8frr7mit2x26od8h3z9thk4gz"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-2"
        }
      }, {
        "name" : "hdfs-DATANODE-bd3d7eb41c2bd0bd33632df5f6dd504a",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-0acae7e6fe7ad4f40"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "61zqh5jng8ivljarhs54nh636"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-1"
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-42d49814318c11e43c1e4054e616215f",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-093a5047b66ade686"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8db7vo91etn4fmeq1ej5t8uuu"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-FAILOVERCONTROLLER-BASE"
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-b174f6d748bb2e785de46822c2491c1e",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-0fb0c30f993032b36"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dhlceog5tdl784h1mpx4sg16x"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-FAILOVERCONTROLLER-BASE"
        }
      }, {
        "name" : "hdfs-GATEWAY-55ada182df2a511076bcf7535a2b966e",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0be3621b8aef0a06a"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-GATEWAY-BASE"
        }
      }, {
        "name" : "hdfs-HTTPFS-d78e8ec89a6e80b5cdfa18d7fa49b600",
        "type" : "HTTPFS",
        "hostRef" : {
          "hostId" : "i-054e4fabb1c61dd56"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ci6zdj9jrjaighx2kb2ctd9hf"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-HTTPFS-BASE"
        }
      }, {
        "name" : "hdfs-JOURNALNODE-b174f6d748bb2e785de46822c2491c1e",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-0fb0c30f993032b36"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "60f09l60vnziy2kcnnsw450t8"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-JOURNALNODE-BASE"
        }
      }, {
        "name" : "hdfs-JOURNALNODE-bd3d7eb41c2bd0bd33632df5f6dd504a",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-0acae7e6fe7ad4f40"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6da0piux1ger5145ikx90i7zs"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-JOURNALNODE-BASE"
        }
      }, {
        "name" : "hdfs-JOURNALNODE-d78e8ec89a6e80b5cdfa18d7fa49b600",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-054e4fabb1c61dd56"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "70bdad98ixj2sy9xepqcryek"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-JOURNALNODE-BASE"
        }
      }, {
        "name" : "hdfs-NAMENODE-42d49814318c11e43c1e4054e616215f",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-093a5047b66ade686"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "41"
          }, {
            "name" : "role_jceks_password",
            "value" : "bfdy5pz09iz8ia5afvjky4x9v"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-NAMENODE-BASE"
        }
      }, {
        "name" : "hdfs-NAMENODE-b174f6d748bb2e785de46822c2491c1e",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-0fb0c30f993032b36"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "52"
          }, {
            "name" : "role_jceks_password",
            "value" : "5ytvzzr826wnppvo8lqhrc41a"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-NAMENODE-BASE"
        }
      } ],
      "displayName" : "HDFS",
      "roleConfigGroups" : [ {
        "name" : "hdfs-BALANCER-BASE",
        "displayName" : "Balancer Default Group",
        "roleType" : "BALANCER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-1",
        "displayName" : "DataNode Group 1",
        "roleType" : "DATANODE",
        "base" : false,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1742733312"
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "3170683699"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "5811208192"
          }, {
            "name" : "rm_cpu_shares",
            "value" : "1800"
          }, {
            "name" : "rm_io_weight",
            "value" : "900"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-2",
        "displayName" : "DataNode Group 2",
        "roleType" : "DATANODE",
        "base" : false,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1073741824"
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "3170683699"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-BASE",
        "displayName" : "DataNode Default Group",
        "roleType" : "DATANODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1742733312"
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "3170683699"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "7671382016"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-BASE",
        "displayName" : "Failover Controller Default Group",
        "roleType" : "FAILOVERCONTROLLER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }
      }, {
        "name" : "hdfs-HTTPFS-BASE",
        "displayName" : "HttpFS Default Group",
        "roleType" : "HTTPFS",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-BASE",
        "displayName" : "JournalNode Default Group",
        "roleType" : "JOURNALNODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/dfs/jn"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-BASE",
        "displayName" : "NameNode Default Group",
        "roleType" : "NAMENODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "2154823680"
          } ]
        }
      }, {
        "name" : "hdfs-NFSGATEWAY-BASE",
        "displayName" : "NFS Gateway Default Group",
        "roleType" : "NFSGATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-SECONDARYNAMENODE-BASE",
        "displayName" : "SecondaryNameNode Default Group",
        "roleType" : "SECONDARYNAMENODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "2154823680"
          } ]
        }
      } ],
      "replicationSchedules" : [ {
        "id" : 3,
        "startTime" : "2017-06-07T12:31:33.554Z",
        "interval" : 0,
        "intervalUnit" : "MINUTE",
        "paused" : false,
        "nextRun" : null,
        "alertOnStart" : false,
        "alertOnSuccess" : false,
        "alertOnFail" : false,
        "alertOnAbort" : false,
        "hdfsArguments" : {
          "sourceService" : {
            "peerName" : "majimenez",
            "clusterName" : "cluster",
            "serviceName" : "hdfs"
          },
          "sourcePath" : "/user/majimenez/tera_gen",
          "destinationPath" : "/user/majimenez/tera_gen",
          "mapreduceServiceName" : "yarn",
          "dryRun" : false,
          "abortOnError" : false,
          "removeMissingFiles" : false,
          "preserveReplicationCount" : true,
          "preserveBlockSize" : true,
          "preservePermissions" : true,
          "skipChecksumChecks" : false,
          "skipTrash" : false,
          "replicationStrategy" : "DYNAMIC",
          "preserveXAttrs" : false,
          "exclusionFilters" : [ ]
        },
        "active" : false
      } ],
      "snapshotPolicies" : [ ]
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "10"
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "false"
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "false"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "gH6R5M8PaZjQv5HopbPafx6OxZ2kO3"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-42d49814318c11e43c1e4054e616215f",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "i-093a5047b66ade686"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "auj64nzt1kq7pjt7b43588sp9"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-JOBHISTORY-BASE"
        }
      }, {
        "name" : "yarn-NODEMANAGER-55ada182df2a511076bcf7535a2b966e",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-0be3621b8aef0a06a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "87c71oxy57onfjg7waa87n7s"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-1"
        }
      }, {
        "name" : "yarn-NODEMANAGER-b174f6d748bb2e785de46822c2491c1e",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-0fb0c30f993032b36"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7f4frjlcyemjjdrn5ep11bdwy"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-BASE"
        }
      }, {
        "name" : "yarn-NODEMANAGER-bd3d7eb41c2bd0bd33632df5f6dd504a",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-0acae7e6fe7ad4f40"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "e0c2l1us9s3iurxdqmeemir1n"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-2"
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-42d49814318c11e43c1e4054e616215f",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "i-093a5047b66ade686"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "47"
          }, {
            "name" : "role_jceks_password",
            "value" : "elyomcpmksa3t2ezppiwgiaj0"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-RESOURCEMANAGER-BASE"
        }
      } ],
      "displayName" : "YARN (MR2 Included)",
      "roleConfigGroups" : [ {
        "name" : "yarn-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "6"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "1"
          } ]
        }
      }, {
        "name" : "yarn-JOBHISTORY-BASE",
        "displayName" : "JobHistory Server Default Group",
        "roleType" : "JOBHISTORY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-1",
        "displayName" : "NodeManager Group 1",
        "roleType" : "NODEMANAGER",
        "base" : false,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_cpu_shares",
            "value" : "200"
          }, {
            "name" : "rm_io_weight",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "1"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "1200"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-2",
        "displayName" : "NodeManager Group 2",
        "roleType" : "NODEMANAGER",
        "base" : false,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "4"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "1200"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-BASE",
        "displayName" : "NodeManager Default Group",
        "roleType" : "NODEMANAGER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "4"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "1024"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-BASE",
        "displayName" : "ResourceManager Default Group",
        "roleType" : "RESOURCEMANAGER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "1200"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "1"
          } ]
        }
      } ]
    }, {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-47-133.eu-west-1.compute.internal"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "T3mp0r@l"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-d78e8ec89a6e80b5cdfa18d7fa49b600",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-054e4fabb1c61dd56"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-HIVEMETASTORE-d78e8ec89a6e80b5cdfa18d7fa49b600",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "i-054e4fabb1c61dd56"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6g8t48sij7qtq96zi31skqy8s"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-HIVEMETASTORE-BASE"
        }
      }, {
        "name" : "hive-HIVESERVER2-d78e8ec89a6e80b5cdfa18d7fa49b600",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "i-054e4fabb1c61dd56"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "evtufbicpcoajyr2y9i46qadh"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-HIVESERVER2-BASE"
        }
      } ],
      "displayName" : "Hive",
      "roleConfigGroups" : [ {
        "name" : "hive-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-BASE",
        "displayName" : "Hive Metastore Server Default Group",
        "roleType" : "HIVEMETASTORE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "893386752"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-BASE",
        "displayName" : "HiveServer2 Default Group",
        "roleType" : "HIVESERVER2",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "893386752"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "2380634521"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "400"
          } ]
        }
      }, {
        "name" : "hive-WEBHCAT-BASE",
        "displayName" : "WebHCat Server Default Group",
        "roleType" : "WEBHCAT",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ ]
        }
      } ],
      "replicationSchedules" : [ ]
    } ],
    "parcels" : [ {
      "product" : "CDH",
      "version" : "5.8.3-1.cdh5.8.3.p0.2",
      "stage" : "DISTRIBUTED",
      "clusterRef" : {
        "clusterName" : "cluster"
      }
    }, {
      "product" : "CDH",
      "version" : "5.8.3-1.cdh5.8.3.p0.2",
      "stage" : "ACTIVATED",
      "clusterRef" : {
        "clusterName" : "cluster"
      }
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "i-0fb0c30f993032b36",
    "ipAddress" : "172.31.32.132",
    "hostname" : "ip-172-31-32-132.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-0be3621b8aef0a06a",
    "ipAddress" : "172.31.34.238",
    "hostname" : "ip-172-31-34-238.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-0acae7e6fe7ad4f40",
    "ipAddress" : "172.31.36.216",
    "hostname" : "ip-172-31-36-216.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-093a5047b66ade686",
    "ipAddress" : "172.31.39.40",
    "hostname" : "ip-172-31-39-40.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-054e4fabb1c61dd56",
    "ipAddress" : "172.31.47.133",
    "hostname" : "ip-172-31-47-133.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__f3f7c71f-532d-479a-902d-89974e05e18d",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "d6cca32db2b8d5ce372a4c9ac9d58fc21809a3e4bdf9ddd94944f3b3c54218e0",
    "pwSalt" : 1441054017631288404,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-d78e8ec89a6e80b5cdfa18d7fa49b600",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "07ab661db84866fec20afb0431649674276b61c4db3189c7bf18f8cc6a878b7b",
    "pwSalt" : 6148173461524051457,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-d78e8ec89a6e80b5cdfa18d7fa49b600",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "8e67f127e27ea9bff09ba6f96b18a4d2b86522ae32fe5bbf100394b7e9ed6666",
    "pwSalt" : 3840056590789600713,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-d78e8ec89a6e80b5cdfa18d7fa49b600",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "9b9e9c9473ac4162d8609e9343885b0bc50e6bdeaf57db9a56d25a7fb65048b1",
    "pwSalt" : -3599397717927767591,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-d78e8ec89a6e80b5cdfa18d7fa49b600",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "1f5f6357afb7b9db7b7068c1a2b69695b6bf5a94f447009c3781b4a93adef5b4",
    "pwSalt" : -6441934811436441253,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "2f872e44e5b3fa607cbc855c2d88e395d0ad1e5038fce10757fa60f2031ae4a1",
    "pwSalt" : -633138863655913773,
    "pwLogin" : true
  }, {
    "name" : "ainowy",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "df8ce4b4efcfe113518ea9606d9df9176abdfcb2df94f5a36ae2a856cf3e6312",
    "pwSalt" : -4262776850419261434,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "2c3bfe45b098aca7034ae08605ca7704be1fe1eafe97f2b852f40d68d471b45a",
    "pwSalt" : 5095809812286888479,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.8.3",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20161019-1014",
    "gitHash" : "518f0d6d44abc87bc392646e4369a20c8192b7cf",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-d78e8ec89a6e80b5cdfa18d7fa49b600",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "i-054e4fabb1c61dd56"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "75sz8yognyuw0fw6y90jkok82"
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-ALERTPUBLISHER-BASE"
      }
    }, {
      "name" : "mgmt-EVENTSERVER-d78e8ec89a6e80b5cdfa18d7fa49b600",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "i-054e4fabb1c61dd56"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "a84qkgrmc27ov6lhzyh9xrwnb"
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-EVENTSERVER-BASE"
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-d78e8ec89a6e80b5cdfa18d7fa49b600",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "i-054e4fabb1c61dd56"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "54i72bsfceu5tybz31h47qln5"
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-HOSTMONITOR-BASE"
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-d78e8ec89a6e80b5cdfa18d7fa49b600",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "i-054e4fabb1c61dd56"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "2cxct8df35sof057vobt2d7d3"
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-REPORTSMANAGER-BASE"
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-d78e8ec89a6e80b5cdfa18d7fa49b600",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "i-054e4fabb1c61dd56"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "5m1urfksu8g4ygbm5grwk40xt"
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-SERVICEMONITOR-BASE"
      }
    } ],
    "displayName" : "Cloudera Management Service",
    "roleConfigGroups" : [ {
      "name" : "mgmt-ACTIVITYMONITOR-BASE",
      "displayName" : "Activity Monitor Default Group",
      "roleType" : "ACTIVITYMONITOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-ALERTPUBLISHER-BASE",
      "displayName" : "Alert Publisher Default Group",
      "roleType" : "ALERTPUBLISHER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-BASE",
      "displayName" : "Event Server Default Group",
      "roleType" : "EVENTSERVER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "event_server_heapsize",
          "value" : "893386752"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-BASE",
      "displayName" : "Host Monitor Default Group",
      "roleType" : "HOSTMONITOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "893386752"
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1161822208"
        } ]
      }
    }, {
      "name" : "mgmt-NAVIGATOR-BASE",
      "displayName" : "Navigator Audit Server Default Group",
      "roleType" : "NAVIGATOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-NAVIGATORMETASERVER-BASE",
      "displayName" : "Navigator Metadata Server Default Group",
      "roleType" : "NAVIGATORMETASERVER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-BASE",
      "displayName" : "Reports Manager Default Group",
      "roleType" : "REPORTSMANAGER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-172-31-47-133.eu-west-1.compute.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "T3mp0r@l"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
        }, {
          "name" : "headlamp_heapsize",
          "value" : "893386752"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-BASE",
      "displayName" : "Service Monitor Default Group",
      "roleType" : "SERVICEMONITOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "893386752"
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1161822208"
        } ]
      }
    } ]
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/26/2012 4:30"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/5.8.3/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    } ]
  },
  "allHostsConfig" : {
    "items" : [ {
      "name" : "rm_enabled",
      "value" : "true"
    } ]
  },
  "peers" : [ {
    "name" : "majimenez",
    "type" : "REPLICATION",
    "url" : "http://ec2-34-251-6-22.eu-west-1.compute.amazonaws.com:7180",
    "username" : "__cloudera_internal_user__0b935f88-632f-45dc-9304-22eb1aef705e",
    "password" : "ed60bcc7-84a8-4178-b1a6-7cd94628c534759a74e5-74a2-4702-aef4-f727fbaa78ce",
    "clouderaManagerCreatedUser" : true
  } ],
  "hostTemplates" : {
    "items" : [ ]
  }

</pre>

<pre>
[root@ip-172-31-47-133 ~]# curl -u ainowy:cloudera 'http://34.249.47.205:7180/ai/v12/clusters/ainowy/services/hive/'
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
[root@ip-172-31-47-133 ~]# curl -u ainowy:cloudera 'http://34.249.47.205:7180/api/v12/clusters/ainowy/services/hive/'
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

[root@ip-172-31-47-133 ~]# curl -X POST -u ainowy:cloudera 'http://34.249.47.20:7180/api/v12/clusters/ainowy/services/hive/commands/stop'
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

[root@ip-172-31-47-133 ~]# curl -X POST -u ainowy:cloudera 'http://34.249.47.205:7180/api/v12/clusters/ainowy/services/hive/commands/start'
{
  "id" : 379,
  "name" : "Start",
  "startTime" : "2017-06-07T14:50:58.342Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }

<pre>


</pre>
