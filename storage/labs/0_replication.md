## Distcp from Pankaj's cluster

	hadoop distcp -pb hdfs://52.53.247.180:8020/data/pgaddam /data/pgaddam-clust1
	
	[hdfs@ip-10-0-255-106 root]$ hadoop fs -ls /data/pgaddam-clust1
	Found 2 items
	-rw-r--r--   3 hdfs supergroup          0 2017-03-22 02:35 /data/pgaddam-clust1/_SUCCESS
	drwxr-xr-x   - hdfs supergroup          0 2017-03-22 03:29 /data/pgaddam-clust1/pgaddam

# fsck on the data distcped	
	
	[hdfs@ip-10-0-255-106 root]$ hdfs fsck /data/pgaddam-clust1 -files -blocks
	Connecting to namenode via http://ip-10-0-255-106.us-west-2.compute.internal:50070
	FSCK started by hdfs (auth:SIMPLE) from /10.0.255.106 for path /data/pgaddam-clust1 at Wed Mar 22 05:42:16 UTC 2017
	/data/pgaddam-clust1 <dir>
	/data/pgaddam-clust1/_SUCCESS 0 bytes, 0 block(s):  OK
	
	/data/pgaddam-clust1/pgaddam <dir>
	/data/pgaddam-clust1/pgaddam/_SUCCESS 0 bytes, 0 block(s):  OK
	
	/data/pgaddam-clust1/pgaddam/part-m-00000 500000000 bytes, 15 block(s):  OK
	0. BP-376724358-10.0.255.106-1490148011135:blk_1073743139_2315 len=33554432 Live_repl=3
	1. BP-376724358-10.0.255.106-1490148011135:blk_1073743141_2317 len=33554432 Live_repl=3
	2. BP-376724358-10.0.255.106-1490148011135:blk_1073743142_2318 len=33554432 Live_repl=3
	3. BP-376724358-10.0.255.106-1490148011135:blk_1073743143_2319 len=33554432 Live_repl=3
	4. BP-376724358-10.0.255.106-1490148011135:blk_1073743144_2320 len=33554432 Live_repl=3
	5. BP-376724358-10.0.255.106-1490148011135:blk_1073743145_2321 len=33554432 Live_repl=3
	6. BP-376724358-10.0.255.106-1490148011135:blk_1073743146_2322 len=33554432 Live_repl=3
	7. BP-376724358-10.0.255.106-1490148011135:blk_1073743147_2323 len=33554432 Live_repl=3
	8. BP-376724358-10.0.255.106-1490148011135:blk_1073743148_2324 len=33554432 Live_repl=3
	9. BP-376724358-10.0.255.106-1490148011135:blk_1073743149_2325 len=33554432 Live_repl=3
	10. BP-376724358-10.0.255.106-1490148011135:blk_1073743150_2326 len=33554432 Live_repl=3
	11. BP-376724358-10.0.255.106-1490148011135:blk_1073743151_2327 len=33554432 Live_repl=3
	12. BP-376724358-10.0.255.106-1490148011135:blk_1073743152_2328 len=33554432 Live_repl=3
	13. BP-376724358-10.0.255.106-1490148011135:blk_1073743153_2329 len=33554432 Live_repl=3
	14. BP-376724358-10.0.255.106-1490148011135:blk_1073743154_2330 len=30237952 Live_repl=3
	
	Status: HEALTHY
	 Total size:	500000000 B
	 Total dirs:	2
	 Total files:	3
	 Total symlinks:		0
	 Total blocks (validated):	15 (avg. block size 33333333 B)
	 Minimally replicated blocks:	15 (100.0 %)
	 Over-replicated blocks:	0 (0.0 %)
	 Under-replicated blocks:	0 (0.0 %)
	 Mis-replicated blocks:		0 (0.0 %)
	 Default replication factor:	3
	 Average block replication:	3.0
	 Corrupt blocks:		0
	 Missing replicas:		0 (0.0 %)
	 Number of data-nodes:		4
	 Number of racks:		1
	FSCK ended at Wed Mar 22 05:42:16 UTC 2017 in 3 milliseconds
	
	
	The filesystem under path '/data/pgaddam-clust1' is HEALTHY
		