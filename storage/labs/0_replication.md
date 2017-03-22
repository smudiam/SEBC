## Distcp from Pankaj's cluster

	hadoop distcp -pb hdfs://52.53.247.180:8020/data/pgaddam /data/pgaddam-clust1
	
	[hdfs@ip-10-0-255-106 root]$ hadoop fs -ls /data/pgaddam-clust1
	Found 2 items
	-rw-r--r--   3 hdfs supergroup          0 2017-03-22 02:35 /data/pgaddam-clust1/_SUCCESS
	drwxr-xr-x   - hdfs supergroup          0 2017-03-22 03:29 /data/pgaddam-clust1/pgaddam
	
	