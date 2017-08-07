<p>
[root@ip-172-31-38-126 ~]# curl -u admin:admin http://54.154.59.148:7180/api/v2/cm/deployment
{
  "timestamp" : "2017-08-07T12:59:33.342Z",
  "clusters" : [ {
    "name" : "ainowy",
    "version" : "CDH5",
    "services" : [ {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-5054a9af0ce82a60b6de76b235e4103f",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "2b19b2ff-7879-401e-976d-8248f392c075"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4fnhm9514l57gycck3vntodcj"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-711157dd6459bbc64c2cdbc574d90a24",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "cdd774a1-375b-469f-a040-f53c3e9693ff"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9ozzu7jb7zkv0daf3fkmhyii5"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-feb7a13cfe248ed50e02fb04e1e864f6",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "f3c68124-0eb6-4ed6-af5a-6d2b1cfe547b"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dpmkzepk0tksg48rb6e7q0m7"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "ip-172-31-36-207.eu-west-1.compute.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "T3mp0r@l"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie"
          } ]
        } ],
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
        "name" : "oozie-OOZIE_SERVER-feb7a13cfe248ed50e02fb04e1e864f6",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "f3c68124-0eb6-4ed6-af5a-6d2b1cfe547b"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dqwczek7wftdpcgjkfc5vdn1"
          } ]
        }
      } ],
      "displayName" : "Oozie"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-172-31-36-207.eu-west-1.compute.internal"
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
          "value" : "hdfs-NAMENODE-feb7a13cfe248ed50e02fb04e1e864f6"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-feb7a13cfe248ed50e02fb04e1e864f6",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "f3c68124-0eb6-4ed6-af5a-6d2b1cfe547b"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "npt9iqab00cznoy6n7dzo00r"
          }, {
            "name" : "secret_key",
            "value" : "8CLFKr60tfNhjagDJsXAjDYPTqUPKA"
          } ]
        }
      } ],
      "displayName" : "Hue"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "5284468736"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4201644032"
          } ]
        }, {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "2085617664"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "2085617664"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "7tyOJbz8Mne26dvqijxrMmBdTmU3CW"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "q8QR7oq1TKgambc5qcVPrTRUoVDtwM"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "ZH8c0tLQGYQv1qicGh4YeJte9LNQJI"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-711157dd6459bbc64c2cdbc574d90a24",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "cdd774a1-375b-469f-a040-f53c3e9693ff"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-5054a9af0ce82a60b6de76b235e4103f",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "2b19b2ff-7879-401e-976d-8248f392c075"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4am3iax7zbkj5ttxs7s1bh6gf"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-711157dd6459bbc64c2cdbc574d90a24",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "cdd774a1-375b-469f-a040-f53c3e9693ff"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1hnekdrcqb5e0fbymhgslyxjr"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-d545b9bbba6120d829e3cdbfe9a762b4",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "12e56430-c22b-49a5-9158-307018a7c56e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "jbezo1pmxmis3f9qqx4h1xxl"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-feb7a13cfe248ed50e02fb04e1e864f6",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "f3c68124-0eb6-4ed6-af5a-6d2b1cfe547b"
        },
        "config" : {
          "items" : [ {
            "name" : "namenode_id",
            "value" : "43"
          }, {
            "name" : "role_jceks_password",
            "value" : "4ci0wd0bjsmgshtayh7j7zj7q"
          } ]
        }
      }, {
        "name" : "hdfs-SECONDARYNAMENODE-d545b9bbba6120d829e3cdbfe9a762b4",
        "type" : "SECONDARYNAMENODE",
        "hostRef" : {
          "hostId" : "12e56430-c22b-49a5-9158-307018a7c56e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "520wot1ftg7zbemmxd4h3k23w"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "6"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "1"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
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
            "value" : "4007"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "4007"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "4"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "I2VeyltpSeoctcqgdqs7FJOb5rd4jm"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-d545b9bbba6120d829e3cdbfe9a762b4",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "12e56430-c22b-49a5-9158-307018a7c56e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "61dgfg64yf2udxptjj5hvy0vv"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-5054a9af0ce82a60b6de76b235e4103f",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "2b19b2ff-7879-401e-976d-8248f392c075"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "b87k3nkhi50fp8z2ia762fnax"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-711157dd6459bbc64c2cdbc574d90a24",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "cdd774a1-375b-469f-a040-f53c3e9693ff"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "btf9lztbsmv30z12f24m02ysn"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-d545b9bbba6120d829e3cdbfe9a762b4",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "12e56430-c22b-49a5-9158-307018a7c56e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8ffhhc8z23g3oejiybxo081uy"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-feb7a13cfe248ed50e02fb04e1e864f6",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "f3c68124-0eb6-4ed6-af5a-6d2b1cfe547b"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "49"
          }, {
            "name" : "role_jceks_password",
            "value" : "9r1tmjunajoutrqws4cauek99"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "2085617664"
          }, {
            "name" : "hive_metastore_server_max_message_size",
            "value" : "208561766"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "2085617664"
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
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-36-207.eu-west-1.compute.internal"
        }, {
          "name" : "hive_metastore_database_name",
          "value" : "hive"
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
        "name" : "hive-GATEWAY-5054a9af0ce82a60b6de76b235e4103f",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "2b19b2ff-7879-401e-976d-8248f392c075"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-711157dd6459bbc64c2cdbc574d90a24",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "cdd774a1-375b-469f-a040-f53c3e9693ff"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-c4c4f6a619bbe59afc1611d5aba54ee4",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "261d6e86-a1e5-4aee-a83a-f3c94d085de9"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-d545b9bbba6120d829e3cdbfe9a762b4",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "12e56430-c22b-49a5-9158-307018a7c56e"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-feb7a13cfe248ed50e02fb04e1e864f6",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "f3c68124-0eb6-4ed6-af5a-6d2b1cfe547b"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-feb7a13cfe248ed50e02fb04e1e864f6",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "f3c68124-0eb6-4ed6-af5a-6d2b1cfe547b"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "c4phaja5q0b4j2iyo2kymz7lt"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-feb7a13cfe248ed50e02fb04e1e864f6",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "f3c68124-0eb6-4ed6-af5a-6d2b1cfe547b"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bec8k5mrycbsgsal2y3jbe5ee"
          } ]
        }
      } ],
      "displayName" : "Hive"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "2b19b2ff-7879-401e-976d-8248f392c075",
    "ipAddress" : "172.31.32.121",
    "hostname" : "ip-172-31-32-121.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "cdd774a1-375b-469f-a040-f53c3e9693ff",
    "ipAddress" : "172.31.32.86",
    "hostname" : "ip-172-31-32-86.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "12e56430-c22b-49a5-9158-307018a7c56e",
    "ipAddress" : "172.31.33.23",
    "hostname" : "ip-172-31-33-23.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "f3c68124-0eb6-4ed6-af5a-6d2b1cfe547b",
    "ipAddress" : "172.31.36.207",
    "hostname" : "ip-172-31-36-207.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "261d6e86-a1e5-4aee-a83a-f3c94d085de9",
    "ipAddress" : "172.31.38.126",
    "hostname" : "ip-172-31-38-126.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-c4c4f6a619bbe59afc1611d5aba54ee4",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "20030f6730194a4d5978e62acd2597fc9acba85dbb35b0dc9283caf10cd18df3",
    "pwSalt" : 2737092016992236394,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-c4c4f6a619bbe59afc1611d5aba54ee4",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "888b1aaa7b48ebc16d69dc8fadcf3baf4e0ffd293969ef6043bec8f60cdf9802",
    "pwSalt" : -3621868254977581359,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-c4c4f6a619bbe59afc1611d5aba54ee4",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "29e08b79dbe1df54923963578a6ca79999ebc1166b9cad0835d07626ff52efc8",
    "pwSalt" : -874351056802255812,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-c4c4f6a619bbe59afc1611d5aba54ee4",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "9053e41487f9da488b019397e9631ccf0bfec78defd5eff1744d53aadf4aa0a1",
    "pwSalt" : 2700349583283184580,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "ea8e532f989328884ba5fefb98aa965a017544ea1d7329fe5050872f3fc8fe85",
    "pwSalt" : 1017060350899467078,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "9ad6927a0e251b4e4978dffbf7553eef699926452d4a2f9fe12fcfb00fd279e0",
    "pwSalt" : -8746234484546869086,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.11.1",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20170525-1411",
    "gitHash" : "8adcfb8545cb0a35f590717b2626a9ea04948dae",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-172-31-36-207.eu-west-1.compute.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "T3mp0r@l"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-c4c4f6a619bbe59afc1611d5aba54ee4",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "261d6e86-a1e5-4aee-a83a-f3c94d085de9"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "81ngsffsypckhs38k9rfh3vec"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-c4c4f6a619bbe59afc1611d5aba54ee4",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "261d6e86-a1e5-4aee-a83a-f3c94d085de9"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "2lbvgcfan4jrk04yock3l9nvt"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-c4c4f6a619bbe59afc1611d5aba54ee4",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "261d6e86-a1e5-4aee-a83a-f3c94d085de9"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "7n0y6m27fqingr724q1grcrbp"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-c4c4f6a619bbe59afc1611d5aba54ee4",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "261d6e86-a1e5-4aee-a83a-f3c94d085de9"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "5hbukwohjjj1psw67v17y403z"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-c4c4f6a619bbe59afc1611d5aba54ee4",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "261d6e86-a1e5-4aee-a83a-f3c94d085de9"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "45nn3kivoo6sgv5jouu9mzicz"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/22/2012 0:10"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,http://archive.cloudera.com/kudu/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    } ]
  }
}

</p>
