	
# curl -X POST -u admin:admin 'http://34.208.28.66:7180/api/v1/clusters/smudiam/services/hive/commands/stop'
	{
	  "id" : 359,
	  "name" : "Stop",
	  "startTime" : "2017-03-22T21:01:06.233Z",
	  "active" : true,
	  "serviceRef" : {
	    "clusterName" : "cluster",
	    "serviceName" : "hive"
	  }
	}
# curl -u admin:admin 'http://34.208.28.66:7180/api/v1/clusters/smudiam/services/hive'
	{
	  "name" : "hive",
	  "type" : "HIVE",
	  "clusterRef" : {
	    "clusterName" : "cluster"
	  },
	  "serviceUrl" : "http://ip-10-0-255-106.us-west-2.compute.internal:7180/cmf/serviceRedirect/hive",
	  "serviceState" : "STOPPED",
	  "healthSummary" : "GOOD",
	  "healthChecks" : [ {
	    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
	    "summary" : "GOOD"
	  }, {
	    "name" : "HIVE_HIVESERVER2S_HEALTHY",
	    "summary" : "GOOD"
	  } ],
	  "configStale" : false
	}

# curl -X POST -u admin:admin 'http://34.208.28.66:7180/api/v1/clusters/smudiam/services/hive/commands/start'
	{
	  "id" : 363,
	  "name" : "Start",
	  "startTime" : "2017-03-22T21:04:16.473Z",
	  "active" : true,
	  "serviceRef" : {
	    "clusterName" : "cluster",
	    "serviceName" : "hive"
	  }
	}
# curl -u admin:admin 'http://34.208.28.66:7180/api/v1/clusters/smudiam/services/hive'
	{
	  "name" : "hive",
	  "type" : "HIVE",
	  "clusterRef" : {
	    "clusterName" : "cluster"
	  },
	  "serviceUrl" : "http://ip-10-0-255-106.us-west-2.compute.internal:7180/cmf/serviceRedirect/hive",
	  "serviceState" : "STARTING",
	  "healthSummary" : "DISABLED",
	  "healthChecks" : [ {
	    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
	    "summary" : "DISABLED"
	  }, {
	    "name" : "HIVE_HIVESERVER2S_HEALTHY",
	    "summary" : "DISABLED"
	  } ],
	  "configStale" : false
	}