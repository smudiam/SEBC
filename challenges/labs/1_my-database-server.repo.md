# The hostname of your db server node
	ip-10-0-255-164.us-west-2.compute.internal
# The command and output showing your database server's version
	[root@ip-10-0-255-164 ~]# mysql --user=root -p
	Enter password:
	Welcome to the MySQL monitor.  Commands end with ; or \g.
	Your MySQL connection id is 3
	Server version: 5.5.54-log MySQL Community Server (GPL)
	
	Copyright (c) 2000, 2016, Oracle and/or its affiliates. All rights reserved.
	
	Oracle is a registered trademark of Oracle Corporation and/or its
	affiliates. Other names may be trademarks of their respective
	owners.
	
	Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.
	
	mysql>
# The command and output for listing your databases

	mysql> show databases;
	+--------------------+
	| Database           |
	+--------------------+
	| information_schema |
	| hive               |
	| mysql              |
	| oozie              |
	| performance_schema |
	| rman               |
	| scm                |
	| sentry             |
	+--------------------+
	8 rows in set (0.00 sec)