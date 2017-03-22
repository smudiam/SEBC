####  Teragen command

	sudo -su hdfs hadoop fs -ls /user
	[smudiam@ip-10-0-255-106 centos]$ time hadoop jar hadoop-examples.jar teragen -Dmapred.map.tasks=4 -Ddfs.block.size=33554432 100000000 /user/smudiam/terasort/input
	Not a valid JAR: /tmp/hsperfdata_smudiam/hadoop-examples.jar
	
	real	0m0.215s
	user	0m0.224s
	sys	0m0.063s
	[smudiam@ip-10-0-255-106 centos]$ time hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-examples.jar teragen -Dmapred.map.tasks=4 -Ddfs.block.size=33554432 100000000 /user/smudiam/terasort/input
	17/03/22 07:19:49 INFO client.RMProxy: Connecting to ResourceManager at ip-10-0-255-106.us-west-2.compute.internal/10.0.255.106:8032
	17/03/22 07:19:50 INFO terasort.TeraSort: Generating 100000000 using 4
	17/03/22 07:19:50 INFO mapreduce.JobSubmitter: number of splits:4
	17/03/22 07:19:50 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
	17/03/22 07:19:50 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
	17/03/22 07:19:50 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1490153921136_0003
	17/03/22 07:19:50 INFO impl.YarnClientImpl: Submitted application application_1490153921136_0003
	17/03/22 07:19:50 INFO mapreduce.Job: The url to track the job: http://ip-10-0-255-106.us-west-2.compute.internal:8088/proxy/application_1490153921136_0003/
	17/03/22 07:19:50 INFO mapreduce.Job: Running job: job_1490153921136_0003
	17/03/22 07:19:56 INFO mapreduce.Job: Job job_1490153921136_0003 running in uber mode : false
	17/03/22 07:19:56 INFO mapreduce.Job:  map 0% reduce 0%
	17/03/22 07:20:08 INFO mapreduce.Job:  map 3% reduce 0%
	17/03/22 07:20:11 INFO mapreduce.Job:  map 10% reduce 0%
	17/03/22 07:20:14 INFO mapreduce.Job:  map 14% reduce 0%
	17/03/22 07:20:17 INFO mapreduce.Job:  map 16% reduce 0%
	17/03/22 07:20:20 INFO mapreduce.Job:  map 18% reduce 0%
	17/03/22 07:20:23 INFO mapreduce.Job:  map 20% reduce 0%
	17/03/22 07:20:26 INFO mapreduce.Job:  map 21% reduce 0%
	17/03/22 07:20:29 INFO mapreduce.Job:  map 23% reduce 0%
	17/03/22 07:20:32 INFO mapreduce.Job:  map 24% reduce 0%
	17/03/22 07:20:35 INFO mapreduce.Job:  map 27% reduce 0%
	17/03/22 07:20:38 INFO mapreduce.Job:  map 30% reduce 0%
	17/03/22 07:20:41 INFO mapreduce.Job:  map 33% reduce 0%
	17/03/22 07:20:44 INFO mapreduce.Job:  map 35% reduce 0%
	17/03/22 07:20:50 INFO mapreduce.Job:  map 36% reduce 0%
	17/03/22 07:20:53 INFO mapreduce.Job:  map 39% reduce 0%
	17/03/22 07:20:56 INFO mapreduce.Job:  map 43% reduce 0%
	17/03/22 07:20:59 INFO mapreduce.Job:  map 46% reduce 0%
	17/03/22 07:21:02 INFO mapreduce.Job:  map 49% reduce 0%
	17/03/22 07:21:05 INFO mapreduce.Job:  map 52% reduce 0%
	17/03/22 07:21:08 INFO mapreduce.Job:  map 54% reduce 0%
	17/03/22 07:21:11 INFO mapreduce.Job:  map 56% reduce 0%
	17/03/22 07:21:14 INFO mapreduce.Job:  map 58% reduce 0%
	17/03/22 07:21:17 INFO mapreduce.Job:  map 60% reduce 0%
	17/03/22 07:21:20 INFO mapreduce.Job:  map 62% reduce 0%
	17/03/22 07:21:23 INFO mapreduce.Job:  map 65% reduce 0%
	17/03/22 07:21:26 INFO mapreduce.Job:  map 67% reduce 0%
	17/03/22 07:21:29 INFO mapreduce.Job:  map 69% reduce 0%
	17/03/22 07:21:32 INFO mapreduce.Job:  map 71% reduce 0%
	17/03/22 07:21:35 INFO mapreduce.Job:  map 73% reduce 0%
	17/03/22 07:21:38 INFO mapreduce.Job:  map 76% reduce 0%
	17/03/22 07:21:41 INFO mapreduce.Job:  map 78% reduce 0%
	17/03/22 07:21:44 INFO mapreduce.Job:  map 80% reduce 0%
	17/03/22 07:21:47 INFO mapreduce.Job:  map 82% reduce 0%
	17/03/22 07:21:50 INFO mapreduce.Job:  map 84% reduce 0%
	17/03/22 07:21:53 INFO mapreduce.Job:  map 86% reduce 0%
	17/03/22 07:21:56 INFO mapreduce.Job:  map 88% reduce 0%
	17/03/22 07:21:59 INFO mapreduce.Job:  map 90% reduce 0%
	17/03/22 07:22:02 INFO mapreduce.Job:  map 91% reduce 0%
	17/03/22 07:22:05 INFO mapreduce.Job:  map 94% reduce 0%
	17/03/22 07:22:11 INFO mapreduce.Job:  map 96% reduce 0%
	17/03/22 07:22:14 INFO mapreduce.Job:  map 98% reduce 0%
	17/03/22 07:22:17 INFO mapreduce.Job:  map 99% reduce 0%
	17/03/22 07:22:19 INFO mapreduce.Job:  map 100% reduce 0%
	17/03/22 07:22:19 INFO mapreduce.Job: Job job_1490153921136_0003 completed successfully
	17/03/22 07:22:19 INFO mapreduce.Job: Counters: 31
		File System Counters
			FILE: Number of bytes read=0
			FILE: Number of bytes written=499889
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
			Total time spent by all maps in occupied slots (ms)=528990
			Total time spent by all reduces in occupied slots (ms)=0
			Total time spent by all map tasks (ms)=528990
			Total vcore-seconds taken by all map tasks=528990
			Total megabyte-seconds taken by all map tasks=541685760
		Map-Reduce Framework
			Map input records=100000000
			Map output records=100000000
			Input split bytes=344
			Spilled Records=0
			Failed Shuffles=0
			Merged Map outputs=0
			GC time elapsed (ms)=1125
			CPU time spent (ms)=159070
			Physical memory (bytes) snapshot=1423626240
			Virtual memory (bytes) snapshot=11143364608
			Total committed heap usage (bytes)=1146093568
		org.apache.hadoop.examples.terasort.TeraGen$Counters
			CHECKSUM=214760662691937609
		File Input Format Counters
			Bytes Read=0
		File Output Format Counters
			Bytes Written=10000000000
	
	real	2m32.698s
	user	0m7.407s
	sys	0m0.616s
		
		
##  Tersort command
	[smudiam@ip-10-0-255-106 centos]$ time hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-examples.jar terasort /user/smudiam/terasort/input /user/smudiam/terasort/output
	17/03/22 07:26:14 INFO terasort.TeraSort: starting
	17/03/22 07:26:16 INFO input.FileInputFormat: Total input paths to process : 4
	Spent 221ms computing base-splits.
	Spent 7ms computing TeraScheduler splits.
	Computing input splits took 228ms
	Sampling 10 splits of 300
	Making 8 from 100000 sampled records
	Computing parititions took 716ms
	Spent 979ms computing partitions.
	17/03/22 07:26:16 INFO client.RMProxy: Connecting to ResourceManager at ip-10-0-255-106.us-west-2.compute.internal/10.0.255.106:8032
	17/03/22 07:26:17 INFO mapreduce.JobSubmitter: number of splits:300
	17/03/22 07:26:17 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1490153921136_0004
	17/03/22 07:26:17 INFO impl.YarnClientImpl: Submitted application application_1490153921136_0004
	17/03/22 07:26:17 INFO mapreduce.Job: The url to track the job: http://ip-10-0-255-106.us-west-2.compute.internal:8088/proxy/application_1490153921136_0004/
	17/03/22 07:26:17 INFO mapreduce.Job: Running job: job_1490153921136_0004
	17/03/22 07:26:23 INFO mapreduce.Job: Job job_1490153921136_0004 running in uber mode : false
	17/03/22 07:26:23 INFO mapreduce.Job:  map 0% reduce 0%
	17/03/22 07:26:32 INFO mapreduce.Job:  map 1% reduce 0%
	17/03/22 07:26:34 INFO mapreduce.Job:  map 2% reduce 0%
	17/03/22 07:26:36 INFO mapreduce.Job:  map 4% reduce 0%
	17/03/22 07:26:39 INFO mapreduce.Job:  map 5% reduce 0%
	17/03/22 07:26:41 INFO mapreduce.Job:  map 6% reduce 0%
	17/03/22 07:26:45 INFO mapreduce.Job:  map 7% reduce 0%
	17/03/22 07:26:47 INFO mapreduce.Job:  map 8% reduce 0%
	17/03/22 07:26:48 INFO mapreduce.Job:  map 9% reduce 0%
	17/03/22 07:26:49 INFO mapreduce.Job:  map 10% reduce 0%
	17/03/22 07:26:52 INFO mapreduce.Job:  map 11% reduce 0%
	17/03/22 07:26:58 INFO mapreduce.Job:  map 12% reduce 0%
	17/03/22 07:27:00 INFO mapreduce.Job:  map 14% reduce 0%
	17/03/22 07:27:01 INFO mapreduce.Job:  map 15% reduce 0%
	17/03/22 07:27:05 INFO mapreduce.Job:  map 16% reduce 0%
	17/03/22 07:27:08 INFO mapreduce.Job:  map 17% reduce 0%
	17/03/22 07:27:12 INFO mapreduce.Job:  map 18% reduce 0%
	17/03/22 07:27:13 INFO mapreduce.Job:  map 20% reduce 0%
	17/03/22 07:27:14 INFO mapreduce.Job:  map 21% reduce 0%
	17/03/22 07:27:18 INFO mapreduce.Job:  map 22% reduce 0%
	17/03/22 07:27:22 INFO mapreduce.Job:  map 23% reduce 0%
	17/03/22 07:27:24 INFO mapreduce.Job:  map 24% reduce 0%
	17/03/22 07:27:25 INFO mapreduce.Job:  map 25% reduce 0%
	17/03/22 07:27:26 INFO mapreduce.Job:  map 26% reduce 0%
	17/03/22 07:27:29 INFO mapreduce.Job:  map 27% reduce 0%
	17/03/22 07:27:34 INFO mapreduce.Job:  map 28% reduce 0%
	17/03/22 07:27:35 INFO mapreduce.Job:  map 29% reduce 0%
	17/03/22 07:27:36 INFO mapreduce.Job:  map 30% reduce 0%
	17/03/22 07:27:38 INFO mapreduce.Job:  map 31% reduce 0%
	17/03/22 07:27:40 INFO mapreduce.Job:  map 32% reduce 0%
	17/03/22 07:27:42 INFO mapreduce.Job:  map 33% reduce 0%
	17/03/22 07:27:48 INFO mapreduce.Job:  map 35% reduce 0%
	17/03/22 07:27:49 INFO mapreduce.Job:  map 36% reduce 0%
	17/03/22 07:27:50 INFO mapreduce.Job:  map 37% reduce 0%
	17/03/22 07:27:55 INFO mapreduce.Job:  map 38% reduce 0%
	17/03/22 07:27:57 INFO mapreduce.Job:  map 39% reduce 0%
	17/03/22 07:27:59 INFO mapreduce.Job:  map 40% reduce 0%
	17/03/22 07:28:01 INFO mapreduce.Job:  map 41% reduce 0%
	17/03/22 07:28:04 INFO mapreduce.Job:  map 42% reduce 0%
	17/03/22 07:28:05 INFO mapreduce.Job:  map 43% reduce 0%
	17/03/22 07:28:11 INFO mapreduce.Job:  map 44% reduce 0%
	17/03/22 07:28:12 INFO mapreduce.Job:  map 45% reduce 0%
	17/03/22 07:28:13 INFO mapreduce.Job:  map 46% reduce 0%
	17/03/22 07:28:14 INFO mapreduce.Job:  map 47% reduce 0%
	17/03/22 07:28:16 INFO mapreduce.Job:  map 48% reduce 0%
	17/03/22 07:28:21 INFO mapreduce.Job:  map 49% reduce 0%
	17/03/22 07:28:23 INFO mapreduce.Job:  map 50% reduce 0%
	17/03/22 07:28:24 INFO mapreduce.Job:  map 51% reduce 0%
	17/03/22 07:28:25 INFO mapreduce.Job:  map 52% reduce 0%
	17/03/22 07:28:27 INFO mapreduce.Job:  map 53% reduce 0%
	17/03/22 07:28:32 INFO mapreduce.Job:  map 54% reduce 0%
	17/03/22 07:28:34 INFO mapreduce.Job:  map 55% reduce 0%
	17/03/22 07:28:35 INFO mapreduce.Job:  map 56% reduce 0%
	17/03/22 07:28:37 INFO mapreduce.Job:  map 57% reduce 0%
	17/03/22 07:28:38 INFO mapreduce.Job:  map 58% reduce 0%
	17/03/22 07:28:41 INFO mapreduce.Job:  map 59% reduce 0%
	17/03/22 07:28:45 INFO mapreduce.Job:  map 60% reduce 0%
	17/03/22 07:28:46 INFO mapreduce.Job:  map 61% reduce 0%
	17/03/22 07:28:47 INFO mapreduce.Job:  map 62% reduce 0%
	17/03/22 07:28:51 INFO mapreduce.Job:  map 63% reduce 0%
	17/03/22 07:28:53 INFO mapreduce.Job:  map 64% reduce 0%
	17/03/22 07:28:55 INFO mapreduce.Job:  map 65% reduce 0%
	17/03/22 07:28:57 INFO mapreduce.Job:  map 66% reduce 0%
	17/03/22 07:28:59 INFO mapreduce.Job:  map 67% reduce 0%
	17/03/22 07:29:02 INFO mapreduce.Job:  map 68% reduce 0%
	17/03/22 07:29:04 INFO mapreduce.Job:  map 69% reduce 0%
	17/03/22 07:29:07 INFO mapreduce.Job:  map 70% reduce 0%
	17/03/22 07:29:09 INFO mapreduce.Job:  map 71% reduce 0%
	17/03/22 07:29:11 INFO mapreduce.Job:  map 72% reduce 0%
	17/03/22 07:29:14 INFO mapreduce.Job:  map 73% reduce 0%
	17/03/22 07:29:15 INFO mapreduce.Job:  map 74% reduce 0%
	17/03/22 07:29:18 INFO mapreduce.Job:  map 75% reduce 0%
	17/03/22 07:29:21 INFO mapreduce.Job:  map 76% reduce 0%
	17/03/22 07:29:22 INFO mapreduce.Job:  map 77% reduce 0%
	17/03/22 07:29:23 INFO mapreduce.Job:  map 78% reduce 0%
	17/03/22 07:29:28 INFO mapreduce.Job:  map 79% reduce 0%
	17/03/22 07:29:29 INFO mapreduce.Job:  map 80% reduce 0%
	17/03/22 07:29:31 INFO mapreduce.Job:  map 81% reduce 0%
	17/03/22 07:29:32 INFO mapreduce.Job:  map 82% reduce 0%
	17/03/22 07:29:36 INFO mapreduce.Job:  map 83% reduce 0%
	17/03/22 07:29:39 INFO mapreduce.Job:  map 84% reduce 0%
	17/03/22 07:29:41 INFO mapreduce.Job:  map 85% reduce 0%
	17/03/22 07:29:43 INFO mapreduce.Job:  map 85% reduce 2%
		17/03/22 07:29:45 INFO mapreduce.Job:  map 85% reduce 5%
		17/03/22 07:29:46 INFO mapreduce.Job:  map 85% reduce 11%
		17/03/22 07:29:47 INFO mapreduce.Job:  map 85% reduce 12%
		17/03/22 07:29:48 INFO mapreduce.Job:  map 85% reduce 14%
		17/03/22 07:29:49 INFO mapreduce.Job:  map 86% reduce 15%
		17/03/22 07:29:50 INFO mapreduce.Job:  map 86% reduce 16%
		17/03/22 07:29:51 INFO mapreduce.Job:  map 86% reduce 17%
		17/03/22 07:29:52 INFO mapreduce.Job:  map 87% reduce 20%
		17/03/22 07:29:53 INFO mapreduce.Job:  map 87% reduce 21%
		17/03/22 07:29:54 INFO mapreduce.Job:  map 87% reduce 22%
		17/03/22 07:29:55 INFO mapreduce.Job:  map 87% reduce 23%
		17/03/22 07:29:56 INFO mapreduce.Job:  map 88% reduce 23%
		17/03/22 07:29:57 INFO mapreduce.Job:  map 88% reduce 25%
		17/03/22 07:30:00 INFO mapreduce.Job:  map 88% reduce 26%
		17/03/22 07:30:02 INFO mapreduce.Job:  map 89% reduce 26%
		17/03/22 07:30:03 INFO mapreduce.Job:  map 90% reduce 26%
		17/03/22 07:30:08 INFO mapreduce.Job:  map 91% reduce 26%
		17/03/22 07:30:11 INFO mapreduce.Job:  map 92% reduce 27%
		17/03/22 07:30:13 INFO mapreduce.Job:  map 93% reduce 27%
		17/03/22 07:30:18 INFO mapreduce.Job:  map 94% reduce 27%
		17/03/22 07:30:20 INFO mapreduce.Job:  map 95% reduce 27%
		17/03/22 07:30:22 INFO mapreduce.Job:  map 95% reduce 28%
		17/03/22 07:30:23 INFO mapreduce.Job:  map 96% reduce 28%
		17/03/22 07:30:28 INFO mapreduce.Job:  map 97% reduce 28%
		17/03/22 07:30:30 INFO mapreduce.Job:  map 98% reduce 28%
		17/03/22 07:30:32 INFO mapreduce.Job:  map 98% reduce 29%
		17/03/22 07:30:33 INFO mapreduce.Job:  map 99% reduce 29%
		17/03/22 07:30:38 INFO mapreduce.Job:  map 100% reduce 29%
		17/03/22 07:30:40 INFO mapreduce.Job:  map 100% reduce 42%
		17/03/22 07:30:41 INFO mapreduce.Job:  map 100% reduce 47%
		17/03/22 07:30:42 INFO mapreduce.Job:  map 100% reduce 58%
		17/03/22 07:30:43 INFO mapreduce.Job:  map 100% reduce 63%
		17/03/22 07:30:45 INFO mapreduce.Job:  map 100% reduce 64%
		17/03/22 07:30:46 INFO mapreduce.Job:  map 100% reduce 67%
		17/03/22 07:30:48 INFO mapreduce.Job:  map 100% reduce 70%
		17/03/22 07:30:49 INFO mapreduce.Job:  map 100% reduce 74%
		17/03/22 07:30:51 INFO mapreduce.Job:  map 100% reduce 75%
		17/03/22 07:30:52 INFO mapreduce.Job:  map 100% reduce 79%
		17/03/22 07:30:54 INFO mapreduce.Job:  map 100% reduce 85%
		17/03/22 07:30:55 INFO mapreduce.Job:  map 100% reduce 86%
		17/03/22 07:30:57 INFO mapreduce.Job:  map 100% reduce 88%
		17/03/22 07:30:58 INFO mapreduce.Job:  map 100% reduce 89%
		17/03/22 07:31:00 INFO mapreduce.Job:  map 100% reduce 90%
		17/03/22 07:31:01 INFO mapreduce.Job:  map 100% reduce 92%
		17/03/22 07:31:03 INFO mapreduce.Job:  map 100% reduce 93%
		17/03/22 07:31:04 INFO mapreduce.Job:  map 100% reduce 94%
		17/03/22 07:31:06 INFO mapreduce.Job:  map 100% reduce 96%
		17/03/22 07:31:08 INFO mapreduce.Job:  map 100% reduce 97%
		17/03/22 07:31:11 INFO mapreduce.Job:  map 100% reduce 98%
		17/03/22 07:31:14 INFO mapreduce.Job:  map 100% reduce 99%
		17/03/22 07:31:17 INFO mapreduce.Job:  map 100% reduce 100%
		17/03/22 07:31:17 INFO mapreduce.Job: Job job_1490153921136_0004 completed successfully
		17/03/22 07:31:17 INFO mapreduce.Job: Counters: 49
			File System Counters
				FILE: Number of bytes read=4443900080
				FILE: Number of bytes written=8825725773
				FILE: Number of read operations=0
				FILE: Number of large read operations=0
				FILE: Number of write operations=0
				HDFS: Number of bytes read=10000037500
				HDFS: Number of bytes written=10000000000
				HDFS: Number of read operations=924
				HDFS: Number of large read operations=0
				HDFS: Number of write operations=16
			Job Counters
				Launched map tasks=300
				Launched reduce tasks=8
				Data-local map tasks=300
				Total time spent by all maps in occupied slots (ms)=2436878
				Total time spent by all reduces in occupied slots (ms)=679929
				Total time spent by all map tasks (ms)=2436878
				Total time spent by all reduce tasks (ms)=679929
				Total vcore-seconds taken by all map tasks=2436878
				Total vcore-seconds taken by all reduce tasks=679929
				Total megabyte-seconds taken by all map tasks=2495363072
				Total megabyte-seconds taken by all reduce tasks=696247296
			Map-Reduce Framework
				Map input records=100000000
				Map output records=100000000
				Map output bytes=10200000000
				Map output materialized bytes=4342875515
				Input split bytes=37500
				Combine input records=0
				Combine output records=0
				Reduce input groups=100000000
				Reduce shuffle bytes=4342875515
				Reduce input records=100000000
				Reduce output records=100000000
				Spilled Records=200000000
				Shuffled Maps =2400
				Failed Shuffles=0
				Merged Map outputs=2400
				GC time elapsed (ms)=61417
				CPU time spent (ms)=1554740
				Physical memory (bytes) snapshot=147840606208
				Virtual memory (bytes) snapshot=858247774208
				Total committed heap usage (bytes)=155030913024
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
		17/03/22 07:31:17 INFO terasort.TeraSort: done
		
		real	5m3.558s
		user	0m10.190s
		sys	0m0.719s
		
		