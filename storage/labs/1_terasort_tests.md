####  Teragen command
		[hdfs@ip-10-0-255-106 root]$ time hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-examples.jar teragen -Dmapred.map.tasks=4 -Ddfs.block.size=33554432 100000000 /data/terasort/input1
		17/03/22 04:35:30 INFO client.RMProxy: Connecting to ResourceManager at ip-10-0-255-106.us-west-2.compute.internal/10.0.255.106:8032
		17/03/22 04:35:30 INFO terasort.TeraSort: Generating 100000000 using 4
		17/03/22 04:35:31 INFO mapreduce.JobSubmitter: number of splits:4
		17/03/22 04:35:31 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
		17/03/22 04:35:31 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
		17/03/22 04:35:31 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1490153921136_0001
		17/03/22 04:35:31 INFO impl.YarnClientImpl: Submitted application application_1490153921136_0001
		17/03/22 04:35:31 INFO mapreduce.Job: The url to track the job: http://ip-10-0-255-106.us-west-2.compute.internal:8088/proxy/application_1490153921136_0001/
		17/03/22 04:35:31 INFO mapreduce.Job: Running job: job_1490153921136_0001
		17/03/22 04:35:38 INFO mapreduce.Job: Job job_1490153921136_0001 running in uber mode : false
		17/03/22 04:35:38 INFO mapreduce.Job:  map 0% reduce 0%
		17/03/22 04:35:50 INFO mapreduce.Job:  map 3% reduce 0%
		17/03/22 04:35:53 INFO mapreduce.Job:  map 4% reduce 0%
		17/03/22 04:35:54 INFO mapreduce.Job:  map 11% reduce 0%
		17/03/22 04:35:56 INFO mapreduce.Job:  map 12% reduce 0%
		17/03/22 04:35:57 INFO mapreduce.Job:  map 14% reduce 0%
		17/03/22 04:35:59 INFO mapreduce.Job:  map 15% reduce 0%
		17/03/22 04:36:00 INFO mapreduce.Job:  map 16% reduce 0%
		17/03/22 04:36:02 INFO mapreduce.Job:  map 17% reduce 0%
		17/03/22 04:36:03 INFO mapreduce.Job:  map 18% reduce 0%
		17/03/22 04:36:05 INFO mapreduce.Job:  map 19% reduce 0%
		17/03/22 04:36:06 INFO mapreduce.Job:  map 21% reduce 0%
		17/03/22 04:36:08 INFO mapreduce.Job:  map 22% reduce 0%
		17/03/22 04:36:09 INFO mapreduce.Job:  map 24% reduce 0%
		17/03/22 04:36:12 INFO mapreduce.Job:  map 26% reduce 0%
		17/03/22 04:36:15 INFO mapreduce.Job:  map 28% reduce 0%
		17/03/22 04:36:18 INFO mapreduce.Job:  map 29% reduce 0%
		17/03/22 04:36:20 INFO mapreduce.Job:  map 30% reduce 0%
		17/03/22 04:36:21 INFO mapreduce.Job:  map 31% reduce 0%
		17/03/22 04:36:24 INFO mapreduce.Job:  map 32% reduce 0%
		17/03/22 04:36:26 INFO mapreduce.Job:  map 33% reduce 0%
		17/03/22 04:36:27 INFO mapreduce.Job:  map 35% reduce 0%
		17/03/22 04:36:29 INFO mapreduce.Job:  map 36% reduce 0%
		17/03/22 04:36:30 INFO mapreduce.Job:  map 37% reduce 0%
		17/03/22 04:36:33 INFO mapreduce.Job:  map 38% reduce 0%
		17/03/22 04:36:35 INFO mapreduce.Job:  map 39% reduce 0%
		17/03/22 04:36:36 INFO mapreduce.Job:  map 41% reduce 0%
		17/03/22 04:36:38 INFO mapreduce.Job:  map 43% reduce 0%
		17/03/22 04:36:39 INFO mapreduce.Job:  map 46% reduce 0%
		17/03/22 04:36:41 INFO mapreduce.Job:  map 47% reduce 0%
		17/03/22 04:36:42 INFO mapreduce.Job:  map 48% reduce 0%
		17/03/22 04:36:44 INFO mapreduce.Job:  map 49% reduce 0%
		17/03/22 04:36:45 INFO mapreduce.Job:  map 51% reduce 0%
		17/03/22 04:36:48 INFO mapreduce.Job:  map 53% reduce 0%
		17/03/22 04:36:54 INFO mapreduce.Job:  map 55% reduce 0%
		17/03/22 04:36:56 INFO mapreduce.Job:  map 56% reduce 0%
		17/03/22 04:36:57 INFO mapreduce.Job:  map 58% reduce 0%
		17/03/22 04:36:59 INFO mapreduce.Job:  map 59% reduce 0%
		17/03/22 04:37:00 INFO mapreduce.Job:  map 61% reduce 0%
		17/03/22 04:37:02 INFO mapreduce.Job:  map 62% reduce 0%
		17/03/22 04:37:03 INFO mapreduce.Job:  map 64% reduce 0%
		17/03/22 04:37:05 INFO mapreduce.Job:  map 65% reduce 0%
		17/03/22 04:37:06 INFO mapreduce.Job:  map 66% reduce 0%
		17/03/22 04:37:08 INFO mapreduce.Job:  map 67% reduce 0%
		17/03/22 04:37:09 INFO mapreduce.Job:  map 68% reduce 0%
		17/03/22 04:37:12 INFO mapreduce.Job:  map 70% reduce 0%
		17/03/22 04:37:14 INFO mapreduce.Job:  map 71% reduce 0%
		17/03/22 04:37:17 INFO mapreduce.Job:  map 72% reduce 0%
		17/03/22 04:37:18 INFO mapreduce.Job:  map 73% reduce 0%
		17/03/22 04:37:21 INFO mapreduce.Job:  map 75% reduce 0%
		17/03/22 04:37:23 INFO mapreduce.Job:  map 76% reduce 0%
		17/03/22 04:37:24 INFO mapreduce.Job:  map 77% reduce 0%
		17/03/22 04:37:26 INFO mapreduce.Job:  map 78% reduce 0%
		17/03/22 04:37:27 INFO mapreduce.Job:  map 80% reduce 0%
		17/03/22 04:37:28 INFO mapreduce.Job:  map 81% reduce 0%
		17/03/22 04:37:30 INFO mapreduce.Job:  map 83% reduce 0%
		17/03/22 04:37:33 INFO mapreduce.Job:  map 85% reduce 0%
		17/03/22 04:37:36 INFO mapreduce.Job:  map 86% reduce 0%
		17/03/22 04:37:39 INFO mapreduce.Job:  map 88% reduce 0%
		17/03/22 04:37:42 INFO mapreduce.Job:  map 90% reduce 0%
		17/03/22 04:37:45 INFO mapreduce.Job:  map 92% reduce 0%
		17/03/22 04:37:48 INFO mapreduce.Job:  map 94% reduce 0%
		17/03/22 04:37:51 INFO mapreduce.Job:  map 95% reduce 0%
		17/03/22 04:37:54 INFO mapreduce.Job:  map 97% reduce 0%
		17/03/22 04:37:57 INFO mapreduce.Job:  map 99% reduce 0%
		17/03/22 04:37:59 INFO mapreduce.Job:  map 100% reduce 0%
		17/03/22 04:37:59 INFO mapreduce.Job: Job job_1490153921136_0001 completed successfully
		17/03/22 04:37:59 INFO mapreduce.Job: Counters: 31
			File System Counters
				FILE: Number of bytes read=0
				FILE: Number of bytes written=499765
				FILE: Number of read operations=0
				FILE: Number of large read operations=0
				FILE: Number of write operations=0
				HDFS: Number of bytes read=344
				HDFS: Number of bytes written=10000000000
				HDFS: Number of read operations=16
				HDFS: Number of large read operations=0
				HDFS: Number of write operations=8
			Job Counters
				Launched map tasks=4
				Other local map tasks=4
				Total time spent by all maps in occupied slots (ms)=518521
				Total time spent by all reduces in occupied slots (ms)=0
				Total time spent by all map tasks (ms)=518521
				Total vcore-seconds taken by all map tasks=518521
				Total megabyte-seconds taken by all map tasks=530965504
			Map-Reduce Framework
				Map input records=100000000
				Map output records=100000000
				Input split bytes=344
				Spilled Records=0
				Failed Shuffles=0
				Merged Map outputs=0
				GC time elapsed (ms)=1063
				CPU time spent (ms)=161120
				Physical memory (bytes) snapshot=1417179136
				Virtual memory (bytes) snapshot=11160891392
				Total committed heap usage (bytes)=1040711680
			org.apache.hadoop.examples.terasort.TeraGen$Counters
				CHECKSUM=214760662691937609
			File Input Format Counters
				Bytes Read=0
			File Output Format Counters
				Bytes Written=10000000000
		
		real	2m32.055s
		user	0m7.441s
		sys	0m0.625s
		
		
##  Tersort command
	[hdfs@ip-10-0-255-106 root]$ time hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-examples.jar terasort /data/terasort/input /data/terasort/output
	17/03/22 04:41:28 INFO terasort.TeraSort: starting
	17/03/22 04:41:29 INFO input.FileInputFormat: Total input paths to process : 4
	Spent 235ms computing base-splits.
	Spent 8ms computing TeraScheduler splits.
	Computing input splits took 244ms
	Sampling 10 splits of 300
	Making 8 from 100000 sampled records
	Computing parititions took 869ms
	Spent 1115ms computing partitions.
	17/03/22 04:41:30 INFO client.RMProxy: Connecting to ResourceManager at ip-10-0-255-106.us-west-2.compute.internal/10.0.255.106:8032
	17/03/22 04:41:30 INFO mapreduce.JobSubmitter: number of splits:300
	17/03/22 04:41:31 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1490153921136_0002
	17/03/22 04:41:31 INFO impl.YarnClientImpl: Submitted application application_1490153921136_0002
	17/03/22 04:41:31 INFO mapreduce.Job: The url to track the job: http://ip-10-0-255-106.us-west-2.compute.internal:8088/proxy/application_1490153921136_0002/
	17/03/22 04:41:31 INFO mapreduce.Job: Running job: job_1490153921136_0002
	17/03/22 04:41:37 INFO mapreduce.Job: Job job_1490153921136_0002 running in uber mode : false
	17/03/22 04:41:37 INFO mapreduce.Job:  map 0% reduce 0%
	17/03/22 04:41:45 INFO mapreduce.Job:  map 1% reduce 0%
	17/03/22 04:41:49 INFO mapreduce.Job:  map 3% reduce 0%
	17/03/22 04:41:50 INFO mapreduce.Job:  map 4% reduce 0%
	17/03/22 04:41:53 INFO mapreduce.Job:  map 5% reduce 0%
	17/03/22 04:41:59 INFO mapreduce.Job:  map 6% reduce 0%
	17/03/22 04:42:00 INFO mapreduce.Job:  map 7% reduce 0%
	17/03/22 04:42:03 INFO mapreduce.Job:  map 8% reduce 0%
	17/03/22 04:42:04 INFO mapreduce.Job:  map 9% reduce 0%
	17/03/22 04:42:07 INFO mapreduce.Job:  map 10% reduce 0%
	17/03/22 04:42:08 INFO mapreduce.Job:  map 11% reduce 0%
	17/03/22 04:42:14 INFO mapreduce.Job:  map 13% reduce 0%
	17/03/22 04:42:16 INFO mapreduce.Job:  map 14% reduce 0%
	17/03/22 04:42:17 INFO mapreduce.Job:  map 15% reduce 0%
	17/03/22 04:42:21 INFO mapreduce.Job:  map 16% reduce 0%
	17/03/22 04:42:25 INFO mapreduce.Job:  map 17% reduce 0%
	17/03/22 04:42:26 INFO mapreduce.Job:  map 18% reduce 0%
	17/03/22 04:42:27 INFO mapreduce.Job:  map 19% reduce 0%
	17/03/22 04:42:29 INFO mapreduce.Job:  map 20% reduce 0%
	17/03/22 04:42:30 INFO mapreduce.Job:  map 21% reduce 0%
	17/03/22 04:42:35 INFO mapreduce.Job:  map 22% reduce 0%
	17/03/22 04:42:36 INFO mapreduce.Job:  map 23% reduce 0%
	17/03/22 04:42:39 INFO mapreduce.Job:  map 24% reduce 0%
	17/03/22 04:42:41 INFO mapreduce.Job:  map 25% reduce 0%
	17/03/22 04:42:42 INFO mapreduce.Job:  map 26% reduce 0%
	17/03/22 04:42:47 INFO mapreduce.Job:  map 27% reduce 0%
	17/03/22 04:42:49 INFO mapreduce.Job:  map 29% reduce 0%
	17/03/22 04:42:52 INFO mapreduce.Job:  map 30% reduce 0%
	17/03/22 04:42:53 INFO mapreduce.Job:  map 31% reduce 0%
	17/03/22 04:42:56 INFO mapreduce.Job:  map 32% reduce 0%
	17/03/22 04:43:00 INFO mapreduce.Job:  map 33% reduce 0%
	17/03/22 04:43:02 INFO mapreduce.Job:  map 34% reduce 0%
	17/03/22 04:43:04 INFO mapreduce.Job:  map 35% reduce 0%
	17/03/22 04:43:06 INFO mapreduce.Job:  map 36% reduce 0%
	17/03/22 04:43:10 INFO mapreduce.Job:  map 37% reduce 0%
	17/03/22 04:43:11 INFO mapreduce.Job:  map 38% reduce 0%
	17/03/22 04:43:13 INFO mapreduce.Job:  map 39% reduce 0%
	17/03/22 04:43:18 INFO mapreduce.Job:  map 41% reduce 0%
	17/03/22 04:43:19 INFO mapreduce.Job:  map 42% reduce 0%
	17/03/22 04:43:24 INFO mapreduce.Job:  map 44% reduce 0%
	17/03/22 04:43:26 INFO mapreduce.Job:  map 45% reduce 0%
	17/03/22 04:43:29 INFO mapreduce.Job:  map 46% reduce 0%
	17/03/22 04:43:30 INFO mapreduce.Job:  map 47% reduce 0%
	17/03/22 04:43:34 INFO mapreduce.Job:  map 48% reduce 0%
	17/03/22 04:43:35 INFO mapreduce.Job:  map 49% reduce 0%
	17/03/22 04:43:36 INFO mapreduce.Job:  map 50% reduce 0%
	17/03/22 04:43:41 INFO mapreduce.Job:  map 51% reduce 0%
	17/03/22 04:43:42 INFO mapreduce.Job:  map 52% reduce 0%
	17/03/22 04:43:44 INFO mapreduce.Job:  map 53% reduce 0%
	17/03/22 04:43:46 INFO mapreduce.Job:  map 54% reduce 0%
	17/03/22 04:43:47 INFO mapreduce.Job:  map 55% reduce 0%
	17/03/22 04:43:52 INFO mapreduce.Job:  map 56% reduce 0%
	17/03/22 04:43:54 INFO mapreduce.Job:  map 57% reduce 0%
	17/03/22 04:43:55 INFO mapreduce.Job:  map 58% reduce 0%
	17/03/22 04:43:57 INFO mapreduce.Job:  map 59% reduce 0%
	17/03/22 04:44:00 INFO mapreduce.Job:  map 60% reduce 0%
	17/03/22 04:44:02 INFO mapreduce.Job:  map 61% reduce 0%
	17/03/22 04:44:05 INFO mapreduce.Job:  map 62% reduce 0%
	17/03/22 04:44:07 INFO mapreduce.Job:  map 63% reduce 0%
	17/03/22 04:44:09 INFO mapreduce.Job:  map 64% reduce 0%
	17/03/22 04:44:10 INFO mapreduce.Job:  map 65% reduce 0%
	17/03/22 04:44:12 INFO mapreduce.Job:  map 66% reduce 0%
	17/03/22 04:44:17 INFO mapreduce.Job:  map 67% reduce 0%
	17/03/22 04:44:18 INFO mapreduce.Job:  map 68% reduce 0%
	17/03/22 04:44:20 INFO mapreduce.Job:  map 69% reduce 0%
	17/03/22 04:44:22 INFO mapreduce.Job:  map 70% reduce 0%
	17/03/22 04:44:23 INFO mapreduce.Job:  map 71% reduce 0%
	17/03/22 04:44:29 INFO mapreduce.Job:  map 72% reduce 0%
	17/03/22 04:44:30 INFO mapreduce.Job:  map 73% reduce 0%
	17/03/22 04:44:31 INFO mapreduce.Job:  map 74% reduce 0%
	17/03/22 04:44:33 INFO mapreduce.Job:  map 75% reduce 0%
	17/03/22 04:44:34 INFO mapreduce.Job:  map 76% reduce 0%
	17/03/22 04:44:39 INFO mapreduce.Job:  map 77% reduce 0%
	17/03/22 04:44:41 INFO mapreduce.Job:  map 78% reduce 0%
	17/03/22 04:44:43 INFO mapreduce.Job:  map 79% reduce 0%
	17/03/22 04:44:44 INFO mapreduce.Job:  map 80% reduce 0%
	17/03/22 04:44:46 INFO mapreduce.Job:  map 81% reduce 0%
	17/03/22 04:44:49 INFO mapreduce.Job:  map 82% reduce 0%
	17/03/22 04:44:52 INFO mapreduce.Job:  map 83% reduce 0%
	17/03/22 04:44:54 INFO mapreduce.Job:  map 84% reduce 0%
	17/03/22 04:44:56 INFO mapreduce.Job:  map 85% reduce 0%
	17/03/22 04:44:57 INFO mapreduce.Job:  map 85% reduce 3%
	17/03/22 04:45:01 INFO mapreduce.Job:  map 85% reduce 5%
	17/03/22 04:45:02 INFO mapreduce.Job:  map 85% reduce 9%
	17/03/22 04:45:03 INFO mapreduce.Job:  map 85% reduce 10%
	17/03/22 04:45:04 INFO mapreduce.Job:  map 85% reduce 11%
	17/03/22 04:45:05 INFO mapreduce.Job:  map 85% reduce 15%
	17/03/22 04:45:07 INFO mapreduce.Job:  map 86% reduce 16%
	17/03/22 04:45:08 INFO mapreduce.Job:  map 86% reduce 18%
	17/03/22 04:45:09 INFO mapreduce.Job:  map 87% reduce 18%
	17/03/22 04:45:10 INFO mapreduce.Job:  map 87% reduce 19%
	17/03/22 04:45:11 INFO mapreduce.Job:  map 87% reduce 22%
	17/03/22 04:45:12 INFO mapreduce.Job:  map 87% reduce 23%
	17/03/22 04:45:13 INFO mapreduce.Job:  map 87% reduce 24%
	17/03/22 04:45:17 INFO mapreduce.Job:  map 87% reduce 25%
	17/03/22 04:45:18 INFO mapreduce.Job:  map 88% reduce 25%
	17/03/22 04:45:20 INFO mapreduce.Job:  map 88% reduce 26%
	17/03/22 04:45:21 INFO mapreduce.Job:  map 89% reduce 26%
	17/03/22 04:45:28 INFO mapreduce.Job:  map 90% reduce 26%
	17/03/22 04:45:30 INFO mapreduce.Job:  map 91% reduce 26%
	17/03/22 04:45:33 INFO mapreduce.Job:  map 91% reduce 27%
	17/03/22 04:45:37 INFO mapreduce.Job:  map 92% reduce 27%
	17/03/22 04:45:39 INFO mapreduce.Job:  map 93% reduce 27%
	17/03/22 04:45:45 INFO mapreduce.Job:  map 94% reduce 27%
	17/03/22 04:45:47 INFO mapreduce.Job:  map 95% reduce 27%
	17/03/22 04:45:50 INFO mapreduce.Job:  map 95% reduce 28%
	17/03/22 04:45:54 INFO mapreduce.Job:  map 96% reduce 28%
	17/03/22 04:45:56 INFO mapreduce.Job:  map 97% reduce 28%
	17/03/22 04:46:02 INFO mapreduce.Job:  map 98% reduce 28%
	17/03/22 04:46:05 INFO mapreduce.Job:  map 99% reduce 29%
	17/03/22 04:46:09 INFO mapreduce.Job:  map 100% reduce 29%
	17/03/22 04:46:11 INFO mapreduce.Job:  map 100% reduce 34%
	17/03/22 04:46:12 INFO mapreduce.Job:  map 100% reduce 47%
	17/03/22 04:46:13 INFO mapreduce.Job:  map 100% reduce 51%
	17/03/22 04:46:14 INFO mapreduce.Job:  map 100% reduce 59%
	17/03/22 04:46:15 INFO mapreduce.Job:  map 100% reduce 63%
	17/03/22 04:46:16 INFO mapreduce.Job:  map 100% reduce 64%
	17/03/22 04:46:17 INFO mapreduce.Job:  map 100% reduce 65%
	17/03/22 04:46:18 INFO mapreduce.Job:  map 100% reduce 68%
	17/03/22 04:46:20 INFO mapreduce.Job:  map 100% reduce 70%
	17/03/22 04:46:21 INFO mapreduce.Job:  map 100% reduce 74%
	17/03/22 04:46:22 INFO mapreduce.Job:  map 100% reduce 75%
	17/03/22 04:46:23 INFO mapreduce.Job:  map 100% reduce 77%
	17/03/22 04:46:24 INFO mapreduce.Job:  map 100% reduce 82%
	17/03/22 04:46:25 INFO mapreduce.Job:  map 100% reduce 83%
	17/03/22 04:46:26 INFO mapreduce.Job:  map 100% reduce 85%
	17/03/22 04:46:27 INFO mapreduce.Job:  map 100% reduce 87%
	17/03/22 04:46:28 INFO mapreduce.Job:  map 100% reduce 88%
	17/03/22 04:46:30 INFO mapreduce.Job:  map 100% reduce 89%
	17/03/22 04:46:31 INFO mapreduce.Job:  map 100% reduce 91%
	17/03/22 04:46:33 INFO mapreduce.Job:  map 100% reduce 93%
	17/03/22 04:46:34 INFO mapreduce.Job:  map 100% reduce 94%
	17/03/22 04:46:36 INFO mapreduce.Job:  map 100% reduce 95%
	17/03/22 04:46:37 INFO mapreduce.Job:  map 100% reduce 96%
	17/03/22 04:46:39 INFO mapreduce.Job:  map 100% reduce 97%
	17/03/22 04:46:40 INFO mapreduce.Job:  map 100% reduce 98%
	17/03/22 04:46:41 INFO mapreduce.Job:  map 100% reduce 99%
	17/03/22 04:46:42 INFO mapreduce.Job:  map 100% reduce 100%
	17/03/22 04:46:44 INFO mapreduce.Job: Job job_1490153921136_0002 completed successfully
	17/03/22 04:46:44 INFO mapreduce.Job: Counters: 50
		File System Counters
			FILE: Number of bytes read=4444472982
			FILE: Number of bytes written=8826241401
			FILE: Number of read operations=0
			FILE: Number of large read operations=0
			FILE: Number of write operations=0
			HDFS: Number of bytes read=10000035100
			HDFS: Number of bytes written=10000000000
			HDFS: Number of read operations=924
			HDFS: Number of large read operations=0
			HDFS: Number of write operations=16
		Job Counters
			Launched map tasks=300
			Launched reduce tasks=8
			Data-local map tasks=299
			Rack-local map tasks=1
			Total time spent by all maps in occupied slots (ms)=2579583
			Total time spent by all reduces in occupied slots (ms)=761873
			Total time spent by all map tasks (ms)=2579583
			Total time spent by all reduce tasks (ms)=761873
			Total vcore-seconds taken by all map tasks=2579583
			Total vcore-seconds taken by all reduce tasks=761873
			Total megabyte-seconds taken by all map tasks=2641492992
			Total megabyte-seconds taken by all reduce tasks=780157952
		Map-Reduce Framework
			Map input records=100000000
			Map output records=100000000
			Map output bytes=10200000000
			Map output materialized bytes=4342834453
			Input split bytes=35100
			Combine input records=0
			Combine output records=0
			Reduce input groups=100000000
			Reduce shuffle bytes=4342834453
			Reduce input records=100000000
			Reduce output records=100000000
			Spilled Records=200000000
			Shuffled Maps =2400
			Failed Shuffles=0
			Merged Map outputs=2400
			GC time elapsed (ms)=62317
			CPU time spent (ms)=1570020
			Physical memory (bytes) snapshot=149028745216
			Virtual memory (bytes) snapshot=858184921088
			Total committed heap usage (bytes)=157422190592
		Shuffle Errors
			BAD_ID=0
			CONNECTION=0
			IO_ERROR=0
			WRONG_LENGTH=0
			WRONG_MAP=0
			WRONG_REDUCE=0
		File Input Format Counters
			Bytes Read=10000000000
		File Output Format Counters
			Bytes Written=10000000000
	17/03/22 04:46:44 INFO terasort.TeraSort: done
	
	real	5m17.242s
	user	0m10.354s
	sys	0m0.734s