# curl -u admin:admin 'http://34.208.28.66:7180/api/v2/cm/deployment'

	{
	  "timestamp" : "2017-03-22T21:22:52.755Z",
	  "clusters" : [ {
	    "name" : "smudiam",
	    "version" : "CDH5",
	    "services" : [ {
	      "name" : "zookeeper",
	      "type" : "ZOOKEEPER",
	      "config" : {
	        "roleTypeConfigs" : [ {
	          "roleType" : "SERVER",
	          "items" : [ {
	            "name" : "zookeeper_server_java_heapsize",
	            "value" : "593494016"
	          } ]
	        } ],
	        "items" : [ {
	          "name" : "service_health_suppression_zookeeper_canary_health",
	          "value" : "true"
	        } ]
	      },
	      "roles" : [ {
	        "name" : "zookeeper-SERVER-415e50f0bb1cbdcfaff5665f0710d000",
	        "type" : "SERVER",
	        "hostRef" : {
	          "hostId" : "f15914ca-0203-45d1-93b7-46608059857e"
	        },
	        "config" : {
	          "items" : [ {
	            "name" : "role_jceks_password",
	            "value" : "7c0uaaxkng78hz2rxqxfgsvf4"
	          }, {
	            "name" : "serverId",
	            "value" : "1"
	          } ]
	        }
	      }, {
	        "name" : "zookeeper-SERVER-aa6226276bbff2538be6ea02c7a71238",
	        "type" : "SERVER",
	        "hostRef" : {
	          "hostId" : "ec6e86aa-458e-4357-b381-abe616c70844"
	        },
	        "config" : {
	          "items" : [ {
	            "name" : "role_jceks_password",
	            "value" : "62qhep4j021oob2rvh4d5kmgx"
	          }, {
	            "name" : "serverId",
	            "value" : "3"
	          } ]
	        }
	      }, {
	        "name" : "zookeeper-SERVER-d37dab31bcd199e5147d9cb55d4e7371",
	        "type" : "SERVER",
	        "hostRef" : {
	          "hostId" : "55a2a32f-4e33-42a0-a3ea-56b2ad9a91ac"
	        },
	        "config" : {
	          "items" : [ {
	            "name" : "role_jceks_password",
	            "value" : "834i2d2rvwf62k1am3gebzhzb"
	          }, {
	            "name" : "serverId",
	            "value" : "2"
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
	            "value" : "ip-10-0-255-106.us-west-2.compute.internal"
	          }, {
	            "name" : "oozie_database_password",
	            "value" : "Clairvoyant@123"
	          }, {
	            "name" : "oozie_database_type",
	            "value" : "mysql"
	          }, {
	            "name" : "oozie_database_user",
	            "value" : "oozie"
	          }, {
	            "name" : "oozie_java_heapsize",
	            "value" : "593494016"
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
	        "name" : "oozie-OOZIE_SERVER-415e50f0bb1cbdcfaff5665f0710d000",
	        "type" : "OOZIE_SERVER",
	        "hostRef" : {
	          "hostId" : "f15914ca-0203-45d1-93b7-46608059857e"
	        },
	        "config" : {
	          "items" : [ {
	            "name" : "role_jceks_password",
	            "value" : "7ky4qom8o9doz65qtlczwufjt"
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
	          "value" : "ip-10-0-255-106.us-west-2.compute.internal"
	        }, {
	          "name" : "database_password",
	          "value" : "Clairvoyant@123"
	        }, {
	          "name" : "database_type",
	          "value" : "mysql"
	        }, {
	          "name" : "hive_service",
	          "value" : "hive"
	        }, {
	          "name" : "hue_webhdfs",
	          "value" : "hdfs-NAMENODE-415e50f0bb1cbdcfaff5665f0710d000"
	        }, {
	          "name" : "oozie_service",
	          "value" : "oozie"
	        }, {
	          "name" : "zookeeper_service",
	          "value" : "zookeeper"
	        } ]
	      },
	      "roles" : [ {
	        "name" : "hue-HUE_SERVER-415e50f0bb1cbdcfaff5665f0710d000",
	        "type" : "HUE_SERVER",
	        "hostRef" : {
	          "hostId" : "f15914ca-0203-45d1-93b7-46608059857e"
	        },
	        "config" : {
	          "items" : [ {
	            "name" : "role_jceks_password",
	            "value" : "ckbtp526778a7a7d5zyrcyj4a"
	          }, {
	            "name" : "secret_key",
	            "value" : "1YMeYIQTbht5qfrooLJiQbC7Dud4IE"
	          } ]
	        }
	      } ],
	      "displayName" : "Hue"
	    }, {
	      "name" : "hdfs",
	      "type" : "HDFS",
	      "config" : {
	        "roleTypeConfigs" : [ {
	          "roleType" : "BALANCER",
	          "items" : [ {
	            "name" : "balancer_java_heapsize",
	            "value" : "593494016"
	          } ]
	        }, {
	          "roleType" : "DATANODE",
	          "items" : [ {
	            "name" : "dfs_data_dir_list",
	            "value" : "/dfs/dn,/data/0/dfs/dn,/data/1/dfs/dn"
	          }, {
	            "name" : "dfs_datanode_du_reserved",
	            "value" : "3219866009"
	          }, {
	            "name" : "dfs_datanode_failed_volumes_tolerated",
	            "value" : "1"
	          }, {
	            "name" : "dfs_datanode_max_locked_memory",
	            "value" : "4294967296"
	          } ]
	        }, {
	          "roleType" : "GATEWAY",
	          "items" : [ {
	            "name" : "dfs_client_use_trash",
	            "value" : "true"
	          } ]
	        }, {
	          "roleType" : "JOURNALNODE",
	          "items" : [ {
	            "name" : "dfs_journalnode_edits_dir",
	            "value" : "/dfs/jn"
	          } ]
	        }, {
	          "roleType" : "NAMENODE",
	          "items" : [ {
	            "name" : "dfs_name_dir_list",
	            "value" : "/dfs/nn,/data/0/dfs/nn"
	          }, {
	            "name" : "dfs_namenode_servicerpc_address",
	            "value" : "8022"
	          }, {
	            "name" : "namenode_java_heapsize",
	            "value" : "593494016"
	          } ]
	        }, {
	          "roleType" : "SECONDARYNAMENODE",
	          "items" : [ {
	            "name" : "fs_checkpoint_dir_list",
	            "value" : "/dfs/snn"
	          }, {
	            "name" : "secondary_namenode_java_heapsize",
	            "value" : "593494016"
	          } ]
	        } ],
	        "items" : [ {
	          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
	          "value" : "PzCx6T6ptnhr7xG2ZmMqqBec9H47Op"
	        }, {
	          "name" : "dfs_ha_fencing_methods",
	          "value" : "shell(true)"
	        }, {
	          "name" : "fc_authorization_secret_key",
	          "value" : "T9aidJRVH57K5GcLXixhQxt0udNzH2"
	        }, {
	          "name" : "http_auth_signature_secret",
	          "value" : "W5F1FUgP5qrU12gotm9bDcVKsQNvbM"
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
	        "name" : "hdfs-BALANCER-415e50f0bb1cbdcfaff5665f0710d000",
	        "type" : "BALANCER",
	        "hostRef" : {
	          "hostId" : "f15914ca-0203-45d1-93b7-46608059857e"
	        },
	        "config" : {
	          "items" : [ ]
	        }
	      }, {
	        "name" : "hdfs-DATANODE-95adc04ccf776c290c5e9c9d70d7d3a7",
	        "type" : "DATANODE",
	        "hostRef" : {
	          "hostId" : "de106f57-4d0f-40e6-ace0-96513fb9d06e"
	        },
	        "config" : {
	          "items" : [ {
	            "name" : "role_jceks_password",
	            "value" : "ddk2keb4de1lb1hm3q4i6rych"
	          } ]
	        }
	      }, {
	        "name" : "hdfs-DATANODE-aa6226276bbff2538be6ea02c7a71238",
	        "type" : "DATANODE",
	        "hostRef" : {
	          "hostId" : "ec6e86aa-458e-4357-b381-abe616c70844"
	        },
	        "config" : {
	          "items" : [ {
	            "name" : "role_jceks_password",
	            "value" : "9px2az34iawx74oifndv6k74s"
	          } ]
	        }
	      }, {
	        "name" : "hdfs-DATANODE-d37dab31bcd199e5147d9cb55d4e7371",
	        "type" : "DATANODE",
	        "hostRef" : {
	          "hostId" : "55a2a32f-4e33-42a0-a3ea-56b2ad9a91ac"
	        },
	        "config" : {
	          "items" : [ {
	            "name" : "role_jceks_password",
	            "value" : "5qo2l1js203skuwgwd229wy3n"
	          } ]
	        }
	      }, {
	        "name" : "hdfs-DATANODE-ea3c0b1d774c2986a5ba726dbfcc07a2",
	        "type" : "DATANODE",
	        "hostRef" : {
	          "hostId" : "48d78a21-0014-4024-a709-054b385562e9"
	        },
	        "config" : {
	          "items" : [ {
	            "name" : "role_jceks_password",
	            "value" : "4fk1miofgu67kxxdgr4dbwlrl"
	          } ]
	        }
	      }, {
	        "name" : "hdfs-FAILOVERCONTROLLER-415e50f0bb1cbdcfaff5665f0710d000",
	        "type" : "FAILOVERCONTROLLER",
	        "hostRef" : {
	          "hostId" : "f15914ca-0203-45d1-93b7-46608059857e"
	        },
	        "config" : {
	          "items" : [ {
	            "name" : "role_jceks_password",
	            "value" : "dtxuorsc3otb5qg2zyhywhupk"
	          } ]
	        }
	      }, {
	        "name" : "hdfs-FAILOVERCONTROLLER-aa6226276bbff2538be6ea02c7a71238",
	        "type" : "FAILOVERCONTROLLER",
	        "hostRef" : {
	          "hostId" : "ec6e86aa-458e-4357-b381-abe616c70844"
	        },
	        "config" : {
	          "items" : [ {
	            "name" : "role_jceks_password",
	            "value" : "cw8qogg6s1w80l4mzcy9o599k"
	          } ]
	        }
	      }, {
	        "name" : "hdfs-HTTPFS-aa6226276bbff2538be6ea02c7a71238",
	        "type" : "HTTPFS",
	        "hostRef" : {
	          "hostId" : "ec6e86aa-458e-4357-b381-abe616c70844"
	        },
	        "config" : {
	          "items" : [ {
	            "name" : "role_jceks_password",
	            "value" : "7y92yydad5t92inqywyovcemd"
	          } ]
	        }
	      }, {
	        "name" : "hdfs-JOURNALNODE-415e50f0bb1cbdcfaff5665f0710d000",
	        "type" : "JOURNALNODE",
	        "hostRef" : {
	          "hostId" : "f15914ca-0203-45d1-93b7-46608059857e"
	        },
	        "config" : {
	          "items" : [ {
	            "name" : "role_jceks_password",
	            "value" : "81q4gvmileccc0yo1ez8admjl"
	          } ]
	        }
	      }, {
	        "name" : "hdfs-JOURNALNODE-aa6226276bbff2538be6ea02c7a71238",
	        "type" : "JOURNALNODE",
	        "hostRef" : {
	          "hostId" : "ec6e86aa-458e-4357-b381-abe616c70844"
	        },
	        "config" : {
	          "items" : [ {
	            "name" : "role_jceks_password",
	            "value" : "8siyfg4lr8l7sy546q43lzr2g"
	          } ]
	        }
	      }, {
	        "name" : "hdfs-JOURNALNODE-d37dab31bcd199e5147d9cb55d4e7371",
	        "type" : "JOURNALNODE",
	        "hostRef" : {
	          "hostId" : "55a2a32f-4e33-42a0-a3ea-56b2ad9a91ac"
	        },
	        "config" : {
	          "items" : [ {
	            "name" : "role_jceks_password",
	            "value" : "2ns82ne1ofzyrn2fp0v48y1ym"
	          } ]
	        }
	      }, {
	        "name" : "hdfs-NAMENODE-415e50f0bb1cbdcfaff5665f0710d000",
	        "type" : "NAMENODE",
	        "hostRef" : {
	          "hostId" : "f15914ca-0203-45d1-93b7-46608059857e"
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
	            "value" : "46"
	          }, {
	            "name" : "role_jceks_password",
	            "value" : "1ovwuv7ndiufaidor6zat3xfz"
	          } ]
	        }
	      }, {
	        "name" : "hdfs-NAMENODE-aa6226276bbff2538be6ea02c7a71238",
	        "type" : "NAMENODE",
	        "hostRef" : {
	          "hostId" : "ec6e86aa-458e-4357-b381-abe616c70844"
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
	            "value" : "61"
	          }, {
	            "name" : "role_jceks_password",
	            "value" : "5s658gekh12ank5jf0bd9vxdk"
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
	            "value" : "8"
	          }, {
	            "name" : "mapred_submit_replication",
	            "value" : "2"
	          } ]
	        }, {
	          "roleType" : "JOBHISTORY",
	          "items" : [ {
	            "name" : "mr2_jobhistory_java_heapsize",
	            "value" : "593494016"
	          } ]
	        }, {
	          "roleType" : "NODEMANAGER",
	          "items" : [ {
	            "name" : "yarn_nodemanager_heartbeat_interval_ms",
	            "value" : "100"
	          }, {
	            "name" : "yarn_nodemanager_local_dirs",
	            "value" : "/yarn/nm,/data/0/yarn/nm,/data/1/yarn/nm"
	          }, {
	            "name" : "yarn_nodemanager_log_dirs",
	            "value" : "/yarn/container-logs,/data/0/yarn/container-logs,/data/1/yarn/container-logs"
	          }, {
	            "name" : "yarn_nodemanager_resource_cpu_vcores",
	            "value" : "4"
	          }, {
	            "name" : "yarn_nodemanager_resource_memory_mb",
	            "value" : "4939"
	          } ]
	        }, {
	          "roleType" : "RESOURCEMANAGER",
	          "items" : [ {
	            "name" : "resource_manager_java_heapsize",
	            "value" : "593494016"
	          }, {
	            "name" : "yarn_scheduler_maximum_allocation_mb",
	            "value" : "4939"
	          }, {
	            "name" : "yarn_scheduler_maximum_allocation_vcores",
	            "value" : "3"
	          } ]
	        } ],
	        "items" : [ {
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
	          "value" : "bLBB8Jl9R2h7NqrKDPeXXLTLG8KlGL"
	        }, {
	          "name" : "zookeeper_service",
	          "value" : "zookeeper"
	        } ]
	      },
	      "roles" : [ {
	        "name" : "yarn-JOBHISTORY-415e50f0bb1cbdcfaff5665f0710d000",
	        "type" : "JOBHISTORY",
	        "hostRef" : {
	          "hostId" : "f15914ca-0203-45d1-93b7-46608059857e"
	        },
	        "config" : {
	          "items" : [ {
	            "name" : "role_jceks_password",
	            "value" : "dbojxsba4v864onmmlbydtgax"
	          } ]
	        }
	      }, {
	        "name" : "yarn-NODEMANAGER-95adc04ccf776c290c5e9c9d70d7d3a7",
	        "type" : "NODEMANAGER",
	        "hostRef" : {
	          "hostId" : "de106f57-4d0f-40e6-ace0-96513fb9d06e"
	        },
	        "config" : {
	          "items" : [ {
	            "name" : "role_jceks_password",
	            "value" : "edqi9vcicak3oia2a0u6bbd02"
	          } ]
	        }
	      }, {
	        "name" : "yarn-NODEMANAGER-aa6226276bbff2538be6ea02c7a71238",
	        "type" : "NODEMANAGER",
	        "hostRef" : {
	          "hostId" : "ec6e86aa-458e-4357-b381-abe616c70844"
	        },
	        "config" : {
	          "items" : [ {
	            "name" : "role_jceks_password",
	            "value" : "1shczrhfv8rcyykz1h9hph3wi"
	          } ]
	        }
	      }, {
	        "name" : "yarn-NODEMANAGER-d37dab31bcd199e5147d9cb55d4e7371",
	        "type" : "NODEMANAGER",
	        "hostRef" : {
	          "hostId" : "55a2a32f-4e33-42a0-a3ea-56b2ad9a91ac"
	        },
	        "config" : {
	          "items" : [ {
	            "name" : "role_jceks_password",
	            "value" : "ehgjzzw56xe3zt9o2c5a58hua"
	          } ]
	        }
	      }, {
	        "name" : "yarn-NODEMANAGER-ea3c0b1d774c2986a5ba726dbfcc07a2",
	        "type" : "NODEMANAGER",
	        "hostRef" : {
	          "hostId" : "48d78a21-0014-4024-a709-054b385562e9"
	        },
	        "config" : {
	          "items" : [ {
	            "name" : "role_jceks_password",
	            "value" : "68nmp4x00vxxoi2eib1ltx3yz"
	          } ]
	        }
	      }, {
	        "name" : "yarn-RESOURCEMANAGER-415e50f0bb1cbdcfaff5665f0710d000",
	        "type" : "RESOURCEMANAGER",
	        "hostRef" : {
	          "hostId" : "f15914ca-0203-45d1-93b7-46608059857e"
	        },
	        "config" : {
	          "items" : [ {
	            "name" : "rm_id",
	            "value" : "53"
	          }, {
	            "name" : "role_jceks_password",
	            "value" : "881718fcl06koo13dqxlz9m71"
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
	            "value" : "593494016"
	          } ]
	        }, {
	          "roleType" : "HIVESERVER2",
	          "items" : [ {
	            "name" : "hiveserver2_java_heapsize",
	            "value" : "593494016"
	          }, {
	            "name" : "hiveserver2_spark_driver_memory",
	            "value" : "966367641"
	          }, {
	            "name" : "hiveserver2_spark_executor_cores",
	            "value" : "4"
	          }, {
	            "name" : "hiveserver2_spark_executor_memory",
	            "value" : "3433247539"
	          }, {
	            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
	            "value" : "102"
	          }, {
	            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
	            "value" : "577"
	          } ]
	        } ],
	        "items" : [ {
	          "name" : "hive_metastore_database_host",
	          "value" : "ip-10-0-255-106.us-west-2.compute.internal"
	        }, {
	          "name" : "hive_metastore_database_password",
	          "value" : "Clairvoyant@123"
	        }, {
	          "name" : "mapreduce_yarn_service",
	          "value" : "yarn"
	        }, {
	          "name" : "zookeeper_service",
	          "value" : "zookeeper"
	        } ]
	      },
	      "roles" : [ {
	        "name" : "hive-GATEWAY-415e50f0bb1cbdcfaff5665f0710d000",
	        "type" : "GATEWAY",
	        "hostRef" : {
	          "hostId" : "f15914ca-0203-45d1-93b7-46608059857e"
	        },
	        "config" : {
	          "items" : [ ]
	        }
	      }, {
	        "name" : "hive-GATEWAY-95adc04ccf776c290c5e9c9d70d7d3a7",
	        "type" : "GATEWAY",
	        "hostRef" : {
	          "hostId" : "de106f57-4d0f-40e6-ace0-96513fb9d06e"
	        },
	        "config" : {
	          "items" : [ ]
	        }
	      }, {
	        "name" : "hive-GATEWAY-aa6226276bbff2538be6ea02c7a71238",
	        "type" : "GATEWAY",
	        "hostRef" : {
	          "hostId" : "ec6e86aa-458e-4357-b381-abe616c70844"
	        },
	        "config" : {
	          "items" : [ ]
	        }
	      }, {
	        "name" : "hive-GATEWAY-d37dab31bcd199e5147d9cb55d4e7371",
	        "type" : "GATEWAY",
	        "hostRef" : {
	          "hostId" : "55a2a32f-4e33-42a0-a3ea-56b2ad9a91ac"
	        },
	        "config" : {
	          "items" : [ ]
	        }
	      }, {
	        "name" : "hive-GATEWAY-ea3c0b1d774c2986a5ba726dbfcc07a2",
	        "type" : "GATEWAY",
	        "hostRef" : {
	          "hostId" : "48d78a21-0014-4024-a709-054b385562e9"
	        },
	        "config" : {
	          "items" : [ ]
	        }
	      }, {
	        "name" : "hive-HIVEMETASTORE-415e50f0bb1cbdcfaff5665f0710d000",
	        "type" : "HIVEMETASTORE",
	        "hostRef" : {
	          "hostId" : "f15914ca-0203-45d1-93b7-46608059857e"
	        },
	        "config" : {
	          "items" : [ {
	            "name" : "role_jceks_password",
	            "value" : "5t2723dzcjh8h0u1j8zl5t5rq"
	          } ]
	        }
	      }, {
	        "name" : "hive-HIVESERVER2-415e50f0bb1cbdcfaff5665f0710d000",
	        "type" : "HIVESERVER2",
	        "hostRef" : {
	          "hostId" : "f15914ca-0203-45d1-93b7-46608059857e"
	        },
	        "config" : {
	          "items" : [ {
	            "name" : "role_jceks_password",
	            "value" : "cqzuo5km6nal43iqad8ky79o5"
	          } ]
	        }
	      } ],
	      "displayName" : "Hive"
	    } ]
	  } ],
	  "hosts" : [ {
	    "hostId" : "f15914ca-0203-45d1-93b7-46608059857e",
	    "ipAddress" : "10.0.255.106",
	    "hostname" : "ip-10-0-255-106.us-west-2.compute.internal",
	    "rackId" : "/default",
	    "config" : {
	      "items" : [ ]
	    }
	  }, {
	    "hostId" : "ec6e86aa-458e-4357-b381-abe616c70844",
	    "ipAddress" : "10.0.255.117",
	    "hostname" : "ip-10-0-255-117.us-west-2.compute.internal",
	    "rackId" : "/default",
	    "config" : {
	      "items" : [ ]
	    }
	  }, {
	    "hostId" : "55a2a32f-4e33-42a0-a3ea-56b2ad9a91ac",
	    "ipAddress" : "10.0.255.130",
	    "hostname" : "ip-10-0-255-130.us-west-2.compute.internal",
	    "rackId" : "/default",
	    "config" : {
	      "items" : [ ]
	    }
	  }, {
	    "hostId" : "48d78a21-0014-4024-a709-054b385562e9",
	    "ipAddress" : "10.0.255.214",
	    "hostname" : "ip-10-0-255-214.us-west-2.compute.internal",
	    "rackId" : "/default",
	    "config" : {
	      "items" : [ ]
	    }
	  }, {
	    "hostId" : "de106f57-4d0f-40e6-ace0-96513fb9d06e",
	    "ipAddress" : "10.0.255.47",
	    "hostname" : "ip-10-0-255-47.us-west-2.compute.internal",
	    "rackId" : "/default",
	    "config" : {
	      "items" : [ ]
	    }
	  } ],
	  "users" : [ {
	    "name" : "admin",
	    "roles" : [ "ROLE_CLUSTER_ADMIN" ],
	    "pwHash" : "49dd41aba86dc0e19e1b42ecda445478fcbfc875f30e87e3c8fa53785b7bedc0",
	    "pwSalt" : 2626833647190117913,
	    "pwLogin" : true
	  } ],
	  "versionInfo" : {
	    "version" : "5.9.1",
	    "buildUser" : "jenkins",
	    "buildTimestamp" : "20170112-1158",
	    "gitHash" : "a66d8bbdbe8bc3ee54235e55423f2f76c7d9f3b1",
	    "snapshot" : false
	  },
	  "managementService" : {
	    "name" : "mgmt",
	    "type" : "MGMT",
	    "config" : {
	      "roleTypeConfigs" : [ {
	        "roleType" : "EVENTSERVER",
	        "items" : [ {
	          "name" : "event_server_heapsize",
	          "value" : "593494016"
	        } ]
	      }, {
	        "roleType" : "HOSTMONITOR",
	        "items" : [ {
	          "name" : "firehose_heapsize",
	          "value" : "593494016"
	        }, {
	          "name" : "firehose_non_java_memory_bytes",
	          "value" : "805306368"
	        } ]
	      }, {
	        "roleType" : "REPORTSMANAGER",
	        "items" : [ {
	          "name" : "headlamp_database_host",
	          "value" : "ip-10-0-255-106.us-west-2.compute.internal"
	        }, {
	          "name" : "headlamp_database_name",
	          "value" : "rman"
	        }, {
	          "name" : "headlamp_database_password",
	          "value" : "Clairvoyant@123"
	        }, {
	          "name" : "headlamp_database_user",
	          "value" : "rman"
	        }, {
	          "name" : "headlamp_heapsize",
	          "value" : "593494016"
	        } ]
	      }, {
	        "roleType" : "SERVICEMONITOR",
	        "items" : [ {
	          "name" : "firehose_heapsize",
	          "value" : "593494016"
	        }, {
	          "name" : "firehose_non_java_memory_bytes",
	          "value" : "805306368"
	        } ]
	      } ],
	      "items" : [ ]
	    },
	    "roles" : [ {
	      "name" : "mgmt-ALERTPUBLISHER-415e50f0bb1cbdcfaff5665f0710d000",
	      "type" : "ALERTPUBLISHER",
	      "hostRef" : {
	        "hostId" : "f15914ca-0203-45d1-93b7-46608059857e"
	      },
	      "config" : {
	        "items" : [ {
	          "name" : "role_jceks_password",
	          "value" : "45izrht24y229onmfsvvfk5ve"
	        } ]
	      }
	    }, {
	      "name" : "mgmt-EVENTSERVER-415e50f0bb1cbdcfaff5665f0710d000",
	      "type" : "EVENTSERVER",
	      "hostRef" : {
	        "hostId" : "f15914ca-0203-45d1-93b7-46608059857e"
	      },
	      "config" : {
	        "items" : [ {
	          "name" : "role_jceks_password",
	          "value" : "edvejxbjyk5wkd6l8m2ojg02r"
	        } ]
	      }
	    }, {
	      "name" : "mgmt-HOSTMONITOR-415e50f0bb1cbdcfaff5665f0710d000",
	      "type" : "HOSTMONITOR",
	      "hostRef" : {
	        "hostId" : "f15914ca-0203-45d1-93b7-46608059857e"
	      },
	      "config" : {
	        "items" : [ {
	          "name" : "role_jceks_password",
	          "value" : "20pb639pb9joc1nncdlc302ge"
	        } ]
	      }
	    }, {
	      "name" : "mgmt-REPORTSMANAGER-415e50f0bb1cbdcfaff5665f0710d000",
	      "type" : "REPORTSMANAGER",
	      "hostRef" : {
	        "hostId" : "f15914ca-0203-45d1-93b7-46608059857e"
	      },
	      "config" : {
	        "items" : [ {
	          "name" : "role_jceks_password",
	          "value" : "c9ok4fptkih247unckfk54bow"
	        } ]
	      }
	    }, {
	      "name" : "mgmt-SERVICEMONITOR-415e50f0bb1cbdcfaff5665f0710d000",
	      "type" : "SERVICEMONITOR",
	      "hostRef" : {
	        "hostId" : "f15914ca-0203-45d1-93b7-46608059857e"
	      },
	      "config" : {
	        "items" : [ {
	          "name" : "role_jceks_password",
	          "value" : "9al7xz1pj00s1yrfe05txr8xl"
	        } ]
	      }
	    } ],
	    "displayName" : "Cloudera Management Service"
	  },
	  "managerSettings" : {
	    "items" : [ {
	      "name" : "CLUSTER_STATS_START",
	      "value" : "10/27/2012 3:10"
	    }, {
	      "name" : "PUBLIC_CLOUD_STATUS",
	      "value" : "ON_PUBLIC_CLOUD"
	    }, {
	      "name" : "REMOTE_PARCEL_REPO_URLS",
	      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
	    } ]
	  }
	}
		
