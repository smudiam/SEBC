# curl -u admin:admin 'http://34.208.28.66:7180/api/version'
	v15

# curl -u admin:admin 'http://34.208.28.66:7180/api/v15/cm/version'
	{
	  "version" : "5.10.0",
	  "buildUser" : "jenkins",
	  "buildTimestamp" : "20170120-1037",
	  "gitHash" : "aa0b5cd5eceaefe2f971c13ab657020d96bb842a",
	  "snapshot" : false
	}

# curl -u smudiam:smudiam 'http://34.208.28.66:7180/api/v15/users'
	{
	  "items" : [ {
	    "name" : "admin",
	    "roles" : [ "ROLE_CLUSTER_ADMIN" ]
	  }, {
	    "name" : "minotaur",
	    "roles" : [ "ROLE_CONFIGURATOR" ]
	  }, {
	    "name" : "smudiam",
	    "roles" : [ "ROLE_ADMIN" ]
	  } ]
	}
	
# curl -u admin:admin 'http://34.208.28.66:7180/api/v15/cm/scmDbInfo'
	{
	  "scmDbType" : "MYSQL",
	  "embeddedDbUsed" : false
	}
	
