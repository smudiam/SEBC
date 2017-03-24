# The command and output for hdfs dfs -ls /user
	[root@ip-10-0-255-18 ~]# hdfs dfs -ls /user
	Found 6 items
	drwxr-xr-x   - hdfs   supergroup          0 2017-03-24 18:32 /user/berkeley
	drwxrwxrwx   - mapred hadoop              0 2017-03-24 18:29 /user/history
	drwxrwxr-t   - hive   hive                0 2017-03-24 18:30 /user/hive
	drwxrwxr-x   - hue    hue                 0 2017-03-24 18:30 /user/hue
	drwxrwxr-x   - oozie  oozie               0 2017-03-24 18:31 /user/oozie
	drwxr-xr-x   - hdfs   supergroup          0 2017-03-24 18:32 /user/stanford


# The output from the CM API call ../api/v14/hosts

	Satyas-MacBook-Pro:SEBC satya$ curl -u admin:admin 'http://34.208.107.167:7180/api/v14/hosts'
	{
	  "items" : [ {
	    "hostId" : "f4dcb818-e261-42d6-aac8-cc943dc83cdf",
	    "ipAddress" : "10.0.255.164",
	    "hostname" : "ip-10-0-255-164.us-west-2.compute.internal",
	    "rackId" : "/default",
	    "hostUrl" : "http://ip-10-0-255-18.us-west-2.compute.internal:7180/cmf/hostRedirect/f4dcb818-e261-42d6-aac8-cc943dc83cdf",
	    "maintenanceMode" : false,
	    "maintenanceOwners" : [ ],
	    "commissionState" : "COMMISSIONED",
	    "numCores" : 4,
	    "numPhysicalCores" : 2,
	    "totalPhysMemBytes" : 15331930112
	  }, {
	    "hostId" : "51ca0063-75c6-48ba-bb9f-54e4539e5b71",
	    "ipAddress" : "10.0.255.18",
	    "hostname" : "ip-10-0-255-18.us-west-2.compute.internal",
	    "rackId" : "/default",
	    "hostUrl" : "http://ip-10-0-255-18.us-west-2.compute.internal:7180/cmf/hostRedirect/51ca0063-75c6-48ba-bb9f-54e4539e5b71",
	    "maintenanceMode" : false,
	    "maintenanceOwners" : [ ],
	    "commissionState" : "COMMISSIONED",
	    "numCores" : 4,
	    "numPhysicalCores" : 2,
	    "totalPhysMemBytes" : 15331930112
	  }, {
	    "hostId" : "46dbd60e-e7ff-46d3-ac14-7ae81d8cbf38",
	    "ipAddress" : "10.0.255.194",
	    "hostname" : "ip-10-0-255-194.us-west-2.compute.internal",
	    "rackId" : "/default",
	    "hostUrl" : "http://ip-10-0-255-18.us-west-2.compute.internal:7180/cmf/hostRedirect/46dbd60e-e7ff-46d3-ac14-7ae81d8cbf38",
	    "maintenanceMode" : false,
	    "maintenanceOwners" : [ ],
	    "commissionState" : "COMMISSIONED",
	    "numCores" : 4,
	    "numPhysicalCores" : 2,
	    "totalPhysMemBytes" : 15331930112
	  }, {
	    "hostId" : "9303a976-bb71-452f-8577-d09bc1279f1a",
	    "ipAddress" : "10.0.255.217",
	    "hostname" : "ip-10-0-255-217.us-west-2.compute.internal",
	    "rackId" : "/default",
	    "hostUrl" : "http://ip-10-0-255-18.us-west-2.compute.internal:7180/cmf/hostRedirect/9303a976-bb71-452f-8577-d09bc1279f1a",
	    "maintenanceMode" : false,
	    "maintenanceOwners" : [ ],
	    "commissionState" : "COMMISSIONED",
	    "numCores" : 4,
	    "numPhysicalCores" : 2,
	    "totalPhysMemBytes" : 15331930112
	  }, {
	    "hostId" : "685708c4-1eaa-458d-880c-c1c70b5ef206",
	    "ipAddress" : "10.0.255.220",
	    "hostname" : "ip-10-0-255-220.us-west-2.compute.internal",
	    "rackId" : "/default",
	    "hostUrl" : "http://ip-10-0-255-18.us-west-2.compute.internal:7180/cmf/hostRedirect/685708c4-1eaa-458d-880c-c1c70b5ef206",
	    "maintenanceMode" : false,
	    "maintenanceOwners" : [ ],
	    "commissionState" : "COMMISSIONED",
	    "numCores" : 4,
	    "numPhysicalCores" : 2,
	    "totalPhysMemBytes" : 15331930112
	  } ]
	}Satyas-MacBook-Pro:SEBC satya$