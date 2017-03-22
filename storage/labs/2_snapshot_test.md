# 1. Create a precious directory in HDFS; copy the ZIP course file into it.
	[hdfs@ip-10-0-255-106 root]$ hadoop fs -mkdir /data/precious
	[root@ip-10-0-255-106 ~]# mv /home/centos/SEBC.zip /tmp/
	[root@ip-10-0-255-106 ~]# sudo -su hdfs
	[hdfs@ip-10-0-255-106 root]$ hadoop fs -put /tmp/SEBC.zip /data/precious
	[hdfs@ip-10-0-255-106 root]$ hadoop fs -ls /data/precious
	Found 1 items
	-rw-r--r--   3 hdfs supergroup  165155835 2017-03-22 05:58 /data/precious/SEBC.zip
	
##	Snapshot

	[hdfs@ip-10-0-255-106 root]$ hdfs dfsadmin -allowSnapshot /data/precious
		Allowing snaphot on /data/precious succeeded
	[hdfs@ip-10-0-255-106 root]$ hdfs dfs -createSnapshot /data/precious sebc-hdfs-test
		Created snapshot /data/precious/.snapshot/sebc-hdfs-test
	[hdfs@ip-10-0-255-106 root]$ hdfs dfs -rm -r /data/precious
		rm: Failed to move to trash: hdfs://nameservice1/data/precious: The directory /data/precious cannot be deleted since /data/precious is snapshottable and already has snapshots
		
	[hdfs@ip-10-0-255-106 root]$ hdfs dfs -rm -r /data/precious/SEBC.zip
	17/03/22 06:06:00 INFO fs.TrashPolicyDefault: Moved: 'hdfs://nameservice1/data/precious/SEBC.zip' to trash at: hdfs://nameservice1/user/hdfs/.Trash/Current/data/precious/SEBC.zip
# Restore the deleted file
	[hdfs@ip-10-0-255-106 root]$ hdfs dfs -ls -R /data/precious/.snapshot
	drwxr-xr-x   - hdfs supergroup          0 2017-03-22 06:02 /data/precious/.snapshot/sebc-hdfs-test
	-rw-r--r--   3 hdfs supergroup  165155835 2017-03-22 05:58 /data/precious/.snapshot/sebc-hdfs-test/SEBC.zip
	[hdfs@ip-10-0-255-106 root]$ hdfs dfs -cp /data/precious/.snapshot/sebc-hdfs-test/SEBC.zip /data/precious
	[hdfs@ip-10-0-255-106 root]$ hdfs dfs -ls /data/precious
	Found 1 items
	-rw-r--r--   3 hdfs supergroup  165155835 2017-03-22 06:10 /data/precious/SEBC.zip
