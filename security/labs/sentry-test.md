# beeline
	[root@ip-10-0-255-106 ~]# beeline
	Java HotSpot(TM) 64-Bit Server VM warning: ignoring option MaxPermSize=512M; support was removed in 8.0
	Java HotSpot(TM) 64-Bit Server VM warning: ignoring option MaxPermSize=512M; support was removed in 8.0
	Beeline version 1.1.0-cdh5.10.0 by Apache Hive
	beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-10-0-255-106.us-west-2.compute.internal@SMUDIAM.COM
	scan complete in 2ms
	Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-10-0-255-106.us-west-2.compute.internal@SMUDIAM.COM
	Connected to: Apache Hive (version 1.1.0-cdh5.10.0)
	Driver: Hive JDBC (version 1.1.0-cdh5.10.0)
	Transaction isolation: TRANSACTION_REPEATABLE_READ
	0: jdbc:hive2://localhost:10000/default> show tables;
	INFO  : Compiling command(queryId=hive_20170323191313_1f67b8eb-11e9-41d0-be3b-a9bee47dfef7): show tables
	INFO  : Semantic Analysis Completed
	INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
	INFO  : Completed compiling command(queryId=hive_20170323191313_1f67b8eb-11e9-41d0-be3b-a9bee47dfef7); Time taken: 0.816 seconds
	INFO  : Executing command(queryId=hive_20170323191313_1f67b8eb-11e9-41d0-be3b-a9bee47dfef7): show tables
	INFO  : Starting task [Stage-0:DDL] in serial mode
	INFO  : Completed executing command(queryId=hive_20170323191313_1f67b8eb-11e9-41d0-be3b-a9bee47dfef7); Time taken: 0.252 seconds
	INFO  : OK
	+-----------+--+
	| tab_name  |
	+-----------+--+
	+-----------+--+
	No rows selected (2.634 seconds)
	0: jdbc:hive2://localhost:10000/default>
	
	
# George

	[root@ip-10-0-255-106 ~]# kinit george
	Password for george@SMUDIAM.COM:
	[root@ip-10-0-255-106 ~]# beeline
	Java HotSpot(TM) 64-Bit Server VM warning: ignoring option MaxPermSize=512M; support was removed in 8.0
	Java HotSpot(TM) 64-Bit Server VM warning: ignoring option MaxPermSize=512M; support was removed in 8.0
	Beeline version 1.1.0-cdh5.10.0 by Apache Hive
	beeline> show tables;
	No current connection
	beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-10-0-255-106.us-west-2.compute.internal@SMUDIAM.COM
	scan complete in 2ms
	Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-10-0-255-106.us-west-2.compute.internal@SMUDIAM.COM
	Connected to: Apache Hive (version 1.1.0-cdh5.10.0)
	Driver: Hive JDBC (version 1.1.0-cdh5.10.0)
	Transaction isolation: TRANSACTION_REPEATABLE_READ
	0: jdbc:hive2://localhost:10000/default> show tables;
	INFO  : Compiling command(queryId=hive_20170323193737_b4364df0-7d38-43f0-9764-9d3390b6170c): show tables
	INFO  : Semantic Analysis Completed
	INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
	INFO  : Completed compiling command(queryId=hive_20170323193737_b4364df0-7d38-43f0-9764-9d3390b6170c); Time taken: 0.081 seconds
	INFO  : Executing command(queryId=hive_20170323193737_b4364df0-7d38-43f0-9764-9d3390b6170c): show tables
	INFO  : Starting task [Stage-0:DDL] in serial mode
	INFO  : Completed executing command(queryId=hive_20170323193737_b4364df0-7d38-43f0-9764-9d3390b6170c); Time taken: 0.117 seconds
	INFO  : OK
	+------------+--+
	|  tab_name  |
	+------------+--+
	| customers  |
	| sample_07  |
	| sample_08  |
	| web_logs   |
	+------------+--+
	4 rows selected (0.307 seconds)
	
	
# ferdinand
	
	[centos@ip-10-0-255-106 ~]$ kinit ferdinand
	Password for ferdinand@SMUDIAM.COM:
	[centos@ip-10-0-255-106 ~]$ beeline
	Java HotSpot(TM) 64-Bit Server VM warning: ignoring option MaxPermSize=512M; support was removed in 8.0
	Java HotSpot(TM) 64-Bit Server VM warning: ignoring option MaxPermSize=512M; support was removed in 8.0
	Beeline version 1.1.0-cdh5.10.0 by Apache Hive
	beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-10-0-255-106.us-west-2.compute.internal@SMUDIAM.COM
	scan complete in 2ms
	Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-10-0-255-106.us-west-2.compute.internal@SMUDIAM.COM
	Connected to: Apache Hive (version 1.1.0-cdh5.10.0)
	Driver: Hive JDBC (version 1.1.0-cdh5.10.0)
	Transaction isolation: TRANSACTION_REPEATABLE_READ
	0: jdbc:hive2://localhost:10000/default> show tables;
	INFO  : Compiling command(queryId=hive_20170323194242_0f23b14e-14eb-482c-9a06-5cff9757066f): show tables
	INFO  : Semantic Analysis Completed
	INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
	INFO  : Completed compiling command(queryId=hive_20170323194242_0f23b14e-14eb-482c-9a06-5cff9757066f); Time taken: 0.07 seconds
	INFO  : Executing command(queryId=hive_20170323194242_0f23b14e-14eb-482c-9a06-5cff9757066f): show tables
	INFO  : Starting task [Stage-0:DDL] in serial mode
	INFO  : Completed executing command(queryId=hive_20170323194242_0f23b14e-14eb-482c-9a06-5cff9757066f); Time taken: 0.181 seconds
	INFO  : OK
	+------------+--+
	|  tab_name  |
	+------------+--+
	| sample_07  |
	+------------+--+
	1 row selected (0.37 seconds)
	0: jdbc:hive2://localhost:10000/default>