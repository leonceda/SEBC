*Output of api/v2/cm/deployment resource

```
{
  "timestamp" : "2017-06-07T14:05:10.188Z",
  "clusters" : [ {
    "name" : "Cluster 1",
    "version" : "CDH5",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "1077936128"
          }, {
            "name" : "log_directory_free_space_absolute_thresholds",
            "value" : "{\"warning\":3221225472,\"critical\":1073741824}"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "1077936128"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "1190762905"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "200"
          }, {
            "name" : "log_directory_free_space_absolute_thresholds",
            "value" : "{\"warning\":1073741824,\"critical\":536870912}"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-5-113.eu-west-1.compute.internal"
        }, {
          "name" : "hive_metastore_database_name",
          "value" : "hive"
        }, {
          "name" : "hive_metastore_database_password",
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
        "name" : "hive-GATEWAY-14383f647c0699b6ee765a8d01d0ec29",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "e7830ea9-1973-4584-a454-0c7f0e893caf"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-2fe95d5732ad0521fe602925c288990d",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "fc31636c-b286-44c9-a04b-8085a3a88e46"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-8354d3fb2e592e15ffb7db98af4b6819",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "ac3ca35c-6e2d-4838-8b59-3504013d8110"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-9ab81e807b1c8ed5dc5f258b456e6a23",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "1b3446fa-56f3-4c26-97e3-f9161d9d8e93"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-b59e2e8b1b3505a7bbab507bfa5523ac",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "7c9c1d70-e70e-479f-8de3-9bd13ff50382"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-8354d3fb2e592e15ffb7db98af4b6819",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "ac3ca35c-6e2d-4838-8b59-3504013d8110"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "19vsur3neunhocy6o0yg0orb"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-8354d3fb2e592e15ffb7db98af4b6819",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "ac3ca35c-6e2d-4838-8b59-3504013d8110"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7v3wpb51bivou0zrg4pghiga3"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "SERVER",
          "items" : [ {
            "name" : "dataDir",
            "value" : "/opt/cloudera/zookeeper"
          }, {
            "name" : "dataLogDir",
            "value" : "/opt/cloudera/zookeeper"
          }, {
            "name" : "log_directory_free_space_absolute_thresholds",
            "value" : "{\"warning\":1073741824,\"critical\":536870912}"
          }, {
            "name" : "zookeeper_server_data_directory_free_space_absolute_thresholds",
            "value" : "{\"warning\":1073741824,\"critical\":536870912}"
          } ]
        } ],
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-2fe95d5732ad0521fe602925c288990d",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "fc31636c-b286-44c9-a04b-8085a3a88e46"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6eff4p0tv5xwfoak6592t21dk"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-8354d3fb2e592e15ffb7db98af4b6819",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "ac3ca35c-6e2d-4838-8b59-3504013d8110"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9hspp7zm8o153inelbjmwcizr"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-b59e2e8b1b3505a7bbab507bfa5523ac",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "7c9c1d70-e70e-479f-8de3-9bd13ff50382"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1yfxa1mybv4o9pbcnkbxfvh9e"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HUE_SERVER",
          "items" : [ {
            "name" : "log_directory_free_space_absolute_thresholds",
            "value" : "{\"warning\":3221225472,\"critical\":1073741824}"
          } ]
        } ],
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-172-31-5-113.eu-west-1.compute.internal"
        }, {
          "name" : "database_password",
          "value" : "hue"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-HTTPFS-8354d3fb2e592e15ffb7db98af4b6819"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-2fe95d5732ad0521fe602925c288990d",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "fc31636c-b286-44c9-a04b-8085a3a88e46"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5ofbvkxjqm8v2zeu8gqk0xazr"
          }, {
            "name" : "secret_key",
            "value" : "parzfs3QN6nMxmKYvueBPRgSmUAqvw"
          } ]
        }
      } ],
      "displayName" : "Hue"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "log_directory_free_space_absolute_thresholds",
            "value" : "{\"warning\":3221225472,\"critical\":1073741824}"
          }, {
            "name" : "oozie_data_dir",
            "value" : "/opt/cloudera/oozie/data"
          }, {
            "name" : "oozie_database_host",
            "value" : "ip-172-31-5-113.eu-west-1.compute.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "oozie"
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
        "name" : "oozie-OOZIE_SERVER-2fe95d5732ad0521fe602925c288990d",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "fc31636c-b286-44c9-a04b-8085a3a88e46"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2qcow42ncgch1snueu4veoc2q"
          } ]
        }
      } ],
      "displayName" : "Oozie"
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
            "value" : "2"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "log_directory_free_space_absolute_thresholds",
            "value" : "{\"warning\":1073741824,\"critical\":536870912}"
          }, {
            "name" : "nodemanager_recovery_directory_free_space_absolute_thresholds",
            "value" : "{\"warning\":1073741824,\"critical\":536870912}"
          }, {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/opt/cloudera/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/opt/cloudera/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "4"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "1024"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "log_directory_free_space_absolute_thresholds",
            "value" : "{\"warning\":1073741824,\"critical\":536870912}"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "3253"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "3"
          } ]
        } ],
        "items" : [ {
          "name" : "cm_yarn_container_usage_job_user",
          "value" : "yarn"
        }, {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "90"
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "false"
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "false"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "50ERA8UeZzn3SE6PaITkVpGlcRTpCe"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-GATEWAY-14383f647c0699b6ee765a8d01d0ec29",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "e7830ea9-1973-4584-a454-0c7f0e893caf"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "yarn-GATEWAY-2fe95d5732ad0521fe602925c288990d",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "fc31636c-b286-44c9-a04b-8085a3a88e46"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "yarn-GATEWAY-8354d3fb2e592e15ffb7db98af4b6819",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "ac3ca35c-6e2d-4838-8b59-3504013d8110"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "yarn-GATEWAY-9ab81e807b1c8ed5dc5f258b456e6a23",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "1b3446fa-56f3-4c26-97e3-f9161d9d8e93"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "yarn-GATEWAY-b59e2e8b1b3505a7bbab507bfa5523ac",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "7c9c1d70-e70e-479f-8de3-9bd13ff50382"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "yarn-JOBHISTORY-2fe95d5732ad0521fe602925c288990d",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "fc31636c-b286-44c9-a04b-8085a3a88e46"
        },
        "config" : {
          "items" : [ {
            "name" : "log_directory_free_space_absolute_thresholds",
            "value" : "{\"warning\":1073741824,\"critical\":536870912}"
          }, {
            "name" : "role_jceks_password",
            "value" : "b3h2bnnzl2nlt06tbzydko2ep"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-14383f647c0699b6ee765a8d01d0ec29",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "e7830ea9-1973-4584-a454-0c7f0e893caf"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3knr32te38pvprbg2hqpncwqp"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-2fe95d5732ad0521fe602925c288990d",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "fc31636c-b286-44c9-a04b-8085a3a88e46"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4wj7i82dos17cmk5ty2kvaik2"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-8354d3fb2e592e15ffb7db98af4b6819",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "ac3ca35c-6e2d-4838-8b59-3504013d8110"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "f3p2raabs57inx033g1gi0y01"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-b59e2e8b1b3505a7bbab507bfa5523ac",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "7c9c1d70-e70e-479f-8de3-9bd13ff50382"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "65bf40bb8k250ih0g2925u0eh"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-8354d3fb2e592e15ffb7db98af4b6819",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "ac3ca35c-6e2d-4838-8b59-3504013d8110"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "53"
          }, {
            "name" : "role_jceks_password",
            "value" : "gg7c9ek5m8t4hncbrnfzvrz6"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "dfs_data_dir_list",
            "value" : "/opt/cloudera/dfs/dn"
          }, {
            "name" : "dfs_datanode_data_dir_perm",
            "value" : "755"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "10568941568"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
          }, {
            "name" : "log_directory_free_space_absolute_thresholds",
            "value" : "{\"warning\":1073741824,\"critical\":536870912}"
          } ]
        }, {
          "roleType" : "FAILOVERCONTROLLER",
          "items" : [ {
            "name" : "log_directory_free_space_absolute_thresholds",
            "value" : "{\"warning\":1073741824,\"critical\":536870912}"
          } ]
        }, {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }, {
          "roleType" : "HTTPFS",
          "items" : [ {
            "name" : "log_directory_free_space_absolute_thresholds",
            "value" : "{\"warning\":1073741824,\"critical\":536870912}"
          } ]
        }, {
          "roleType" : "JOURNALNODE",
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/opt/cloudera/dfs/jn"
          }, {
            "name" : "log_directory_free_space_absolute_thresholds",
            "value" : "{\"warning\":1073741824,\"critical\":536870912}"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/opt/cloudera/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "log_directory_free_space_absolute_thresholds",
            "value" : "{\"warning\":1073741824,\"critical\":536870912}"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/opt/cloudera/dfs/snn"
          }, {
            "name" : "log_directory_free_space_absolute_thresholds",
            "value" : "{\"warning\":1073741824,\"critical\":536870912}"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "7WxQwzoF9m5YbMMBakOWgJiBZsDo4L"
        }, {
          "name" : "dfs_ha_fencing_methods",
          "value" : "shell(true)"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "KLoFoMHe8YpWyQIxX9udGiTrf94jkH"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "y7VCj7XKW3961Ls0NAOmM6CKmNxu4t"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "10"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-14383f647c0699b6ee765a8d01d0ec29",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "e7830ea9-1973-4584-a454-0c7f0e893caf"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-14383f647c0699b6ee765a8d01d0ec29",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "e7830ea9-1973-4584-a454-0c7f0e893caf"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8je3sl940743tttx6heixialz"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-2fe95d5732ad0521fe602925c288990d",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "fc31636c-b286-44c9-a04b-8085a3a88e46"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ex8s86m7tpxzd8a8ayb62vue2"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-8354d3fb2e592e15ffb7db98af4b6819",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "ac3ca35c-6e2d-4838-8b59-3504013d8110"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "d3o9o5a9rlxotcdqe3inzpgi8"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-b59e2e8b1b3505a7bbab507bfa5523ac",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "7c9c1d70-e70e-479f-8de3-9bd13ff50382"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_data_dir_list",
            "value" : "/opt/cloudera/dfs/dn"
          }, {
            "name" : "role_jceks_password",
            "value" : "7m7fndgrg58cdyx3xvz2xeuf8"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-14383f647c0699b6ee765a8d01d0ec29",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "e7830ea9-1973-4584-a454-0c7f0e893caf"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6t90lcrlrbhbr05vbczvyr36e"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-8354d3fb2e592e15ffb7db98af4b6819",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "ac3ca35c-6e2d-4838-8b59-3504013d8110"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4trbyu4bkyv9m9mljzrdfi5i5"
          } ]
        }
      }, {
        "name" : "hdfs-GATEWAY-14383f647c0699b6ee765a8d01d0ec29",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "e7830ea9-1973-4584-a454-0c7f0e893caf"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-GATEWAY-2fe95d5732ad0521fe602925c288990d",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "fc31636c-b286-44c9-a04b-8085a3a88e46"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-GATEWAY-8354d3fb2e592e15ffb7db98af4b6819",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "ac3ca35c-6e2d-4838-8b59-3504013d8110"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-GATEWAY-9ab81e807b1c8ed5dc5f258b456e6a23",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "1b3446fa-56f3-4c26-97e3-f9161d9d8e93"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-GATEWAY-b59e2e8b1b3505a7bbab507bfa5523ac",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "7c9c1d70-e70e-479f-8de3-9bd13ff50382"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-HTTPFS-8354d3fb2e592e15ffb7db98af4b6819",
        "type" : "HTTPFS",
        "hostRef" : {
          "hostId" : "ac3ca35c-6e2d-4838-8b59-3504013d8110"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3j137b9lyyikc6lbwtzf6ord0"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-14383f647c0699b6ee765a8d01d0ec29",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "e7830ea9-1973-4584-a454-0c7f0e893caf"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8gmgj29pwlagew1u4l9tsbjqx"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-2fe95d5732ad0521fe602925c288990d",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "fc31636c-b286-44c9-a04b-8085a3a88e46"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6giyc2w7i8pjf8yujb8uwpjwq"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-b59e2e8b1b3505a7bbab507bfa5523ac",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "7c9c1d70-e70e-479f-8de3-9bd13ff50382"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9kna1nmbfo3kxo5uje2v14vtg"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-14383f647c0699b6ee765a8d01d0ec29",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "e7830ea9-1973-4584-a454-0c7f0e893caf"
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
            "value" : "105"
          }, {
            "name" : "role_jceks_password",
            "value" : "asmugnhnabi74eapcdhdk1vln"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-8354d3fb2e592e15ffb7db98af4b6819",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "ac3ca35c-6e2d-4838-8b59-3504013d8110"
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
            "value" : "55"
          }, {
            "name" : "role_jceks_password",
            "value" : "hg2g7sgs10v67q34pdur9ay3"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    }, {
      "name" : "sentry",
      "type" : "SENTRY",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "SENTRY_SERVER",
          "items" : [ {
            "name" : "sentry_server_java_heapsize",
            "value" : "268435456"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "sentry_server_database_host",
          "value" : "ip-172-31-5-113.eu-west-1.compute.internal"
        }, {
          "name" : "sentry_server_database_password",
          "value" : "sentry"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "sentry-GATEWAY-14383f647c0699b6ee765a8d01d0ec29",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "e7830ea9-1973-4584-a454-0c7f0e893caf"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "sentry-GATEWAY-2fe95d5732ad0521fe602925c288990d",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "fc31636c-b286-44c9-a04b-8085a3a88e46"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "sentry-GATEWAY-8354d3fb2e592e15ffb7db98af4b6819",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "ac3ca35c-6e2d-4838-8b59-3504013d8110"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "sentry-GATEWAY-9ab81e807b1c8ed5dc5f258b456e6a23",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "1b3446fa-56f3-4c26-97e3-f9161d9d8e93"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "sentry-GATEWAY-b59e2e8b1b3505a7bbab507bfa5523ac",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "7c9c1d70-e70e-479f-8de3-9bd13ff50382"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "sentry-SENTRY_SERVER-2fe95d5732ad0521fe602925c288990d",
        "type" : "SENTRY_SERVER",
        "hostRef" : {
          "hostId" : "fc31636c-b286-44c9-a04b-8085a3a88e46"
        },
        "config" : {
          "items" : [ {
            "name" : "log_directory_free_space_absolute_thresholds",
            "value" : "{\"warning\":1073741824,\"critical\":536870912}"
          }, {
            "name" : "role_jceks_password",
            "value" : "871hj0kgkrfvai3lq5guqadow"
          } ]
        }
      } ],
      "displayName" : "Sentry"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "e7830ea9-1973-4584-a454-0c7f0e893caf",
    "ipAddress" : "172.31.0.153",
    "hostname" : "ip-172-31-0-153.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "7c9c1d70-e70e-479f-8de3-9bd13ff50382",
    "ipAddress" : "172.31.13.255",
    "hostname" : "ip-172-31-13-255.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "1b3446fa-56f3-4c26-97e3-f9161d9d8e93",
    "ipAddress" : "172.31.5.113",
    "hostname" : "ip-172-31-5-113.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "ac3ca35c-6e2d-4838-8b59-3504013d8110",
    "ipAddress" : "172.31.6.121",
    "hostname" : "ip-172-31-6-121.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "fc31636c-b286-44c9-a04b-8085a3a88e46",
    "ipAddress" : "172.31.8.154",
    "hostname" : "ip-172-31-8-154.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__f13f2d62-2605-4736-849a-b580da73ced4",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "c462bbeab0956254b5241822d5a4f7f7af934ff3769874789adcd7085e0ad1be",
    "pwSalt" : -3315125087570106977,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-9ab81e807b1c8ed5dc5f258b456e6a23",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "7d93e1640941f3ca2a87747ece189dd0c467b674adef3295670053b4385297c3",
    "pwSalt" : 2296930458303527328,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-9ab81e807b1c8ed5dc5f258b456e6a23",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "00fbe5d1296112fc10797d6f7991f06a6cacdca7df3e0e41da08c7c31dd35a9b",
    "pwSalt" : 6656830473768260774,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-9ab81e807b1c8ed5dc5f258b456e6a23",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "6dca4379dd6a1ed5b3e1888165240f76be0fd1004110794c2468b290bd1019d9",
    "pwSalt" : 9105336321519632586,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-9ab81e807b1c8ed5dc5f258b456e6a23",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "c4e276220bdc79370c1c112cd9f6e15f638dc7bc3a21de2fc6fca07efd5af6b9",
    "pwSalt" : -4278514180509195059,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "4cdde0094d2ddf81dbd0e09ebfce304b9f40ae5af1d6b11aeefc6345aec3c05b",
    "pwSalt" : -5059228530842217947,
    "pwLogin" : true
  }, {
    "name" : "bdruser",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "2bc174e00c78e2a4b960ca308560f40192029972d23acba764d97656d37d31f1",
    "pwSalt" : 8589373934118383139,
    "pwLogin" : true
  }, {
    "name" : "leonceda",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "c5290ffe8bb30cca2b95fde653d112e6dfb53d698e1aa26acd57b0a6480bba20",
    "pwSalt" : 2382661889709331664,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_NAVIGATOR_ADMIN" ],
    "pwHash" : "ec093ac79879f1dfcb46fb336882cbad1bc6d1e1c6630d524d61b970d2368366",
    "pwSalt" : 6137697929204720444,
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
      "roleTypeConfigs" : [ {
        "roleType" : "EVENTSERVER",
        "items" : [ {
          "name" : "eventserver_index_dir",
          "value" : "/opt/cloudera/cloudera-scm-eventserver"
        } ]
      }, {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        }, {
          "name" : "firehose_storage_dir",
          "value" : "/opt/cloudera/cloudera-host-monitor"
        } ]
      }, {
        "roleType" : "NAVIGATORMETASERVER",
        "items" : [ {
          "name" : "data_dir",
          "value" : "/opt/cloudera/cloudera-scm-navigator"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-172-31-5-113.eu-west-1.compute.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
        }, {
          "name" : "headlamp_scratch_dir",
          "value" : "/opt/cloudera/cloudera-scm-headlamp"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        }, {
          "name" : "firehose_storage_dir",
          "value" : "/opt/cloudera/cloudera-service-monitor"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-9ab81e807b1c8ed5dc5f258b456e6a23",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "1b3446fa-56f3-4c26-97e3-f9161d9d8e93"
      },
      "config" : {
        "items" : [ {
          "name" : "log_directory_free_space_absolute_thresholds",
          "value" : "{\"warning\":1073741824,\"critical\":536870912}"
        }, {
          "name" : "role_jceks_password",
          "value" : "eyr4kj9ebdhyl1alode5y9hgo"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-9ab81e807b1c8ed5dc5f258b456e6a23",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "1b3446fa-56f3-4c26-97e3-f9161d9d8e93"
      },
      "config" : {
        "items" : [ {
          "name" : "log_directory_free_space_absolute_thresholds",
          "value" : "{\"warning\":1073741824,\"critical\":524288}"
        }, {
          "name" : "role_jceks_password",
          "value" : "2yq3res1biujj2iv6cm2ilc2i"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-9ab81e807b1c8ed5dc5f258b456e6a23",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "1b3446fa-56f3-4c26-97e3-f9161d9d8e93"
      },
      "config" : {
        "items" : [ {
          "name" : "log_directory_free_space_absolute_thresholds",
          "value" : "{\"warning\":1073741824,\"critical\":524288}"
        }, {
          "name" : "role_jceks_password",
          "value" : "7uo968zzdhclbrxyhzjkut5tr"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-9ab81e807b1c8ed5dc5f258b456e6a23",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "1b3446fa-56f3-4c26-97e3-f9161d9d8e93"
      },
      "config" : {
        "items" : [ {
          "name" : "log_directory_free_space_absolute_thresholds",
          "value" : "{\"warning\":1073741824,\"critical\":536870912}"
        }, {
          "name" : "role_jceks_password",
          "value" : "ajfxrptoeq9btrlkahrwu9v92"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-9ab81e807b1c8ed5dc5f258b456e6a23",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "1b3446fa-56f3-4c26-97e3-f9161d9d8e93"
      },
      "config" : {
        "items" : [ {
          "name" : "log_directory_free_space_absolute_thresholds",
          "value" : "{\"warning\":1073741824,\"critical\":536870912}"
        }, {
          "name" : "role_jceks_password",
          "value" : "cv1n4s8cn17odh4z194l8co1x"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/21/2012 20:20"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/,https://archive.cloudera.com/cdh5/parcels/5.8.3/"
    } ]
  }
}
````
