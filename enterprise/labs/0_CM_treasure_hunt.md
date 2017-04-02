* What is ubertask optimization?

	Enabling Enable Ubertask Optimization/ mapreduce.job.ubertask.enable runs sufficiently small mapreduce on the same machine/ single jvm 

* Where in CM is the Kerberos Security Realm value displayed?
	Under Administration => settings => kerberos

* Which CDH service(s) host a property for enabling Kerberos authentication?

	HDFS Service, zookeeper , hive , all services
	
* How do you upgrade the CM agents?

	Hosts => All Hosts => Re-run Upgrade Wizard
	
* Give the tsquery statement used to chart Hue's CPU utilization?

	SELECT total_cpu_percent_across_hosts where $SERVICENAME = hue  $CLUSTERID = 1
	
* Name all the roles that make up the Hive service

	HIVEMETASTORE, HIVESERVER2 
[MFE: Also the Gateway and WebHCatalog]

* What steps must be completed before integrating Cloudera Manager with Kerberos?

	Identify the key distribution center (KDC) that will be used for autnetication that is going to be integrated with Kerberos
[There are other prerequisites listed by the wizard. It is worth knowing them because some customers believe starting the wizard is a point of no return, and so will not see these requirements]	
