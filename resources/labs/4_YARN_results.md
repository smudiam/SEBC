# Slow run

	#!/bin/sh
	# Confirm the path values given below correspond to your installation
	
	MR=/opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce
	HADOOP=/opt/cloudera/parcels/CDH/bin
	
	# Mark start of the loop
	echo Testing loop started on `date`
	
	# Mapper containers
	for i in 8
	do
	   # Reducer containers
	   for j in 1
	   do
	      # Container memory
	      for k in 512 1024
	      do
	         # Set mapper JVM heap
	         MAP_MB=`echo "($k*0.8)/1" | bc`
	
	         # Set reducer JVM heap
	         RED_MB=`echo "($k*0.8)/1" | bc`
		echo ${HADOOP}
		echo $HADOOP
	
	time sudo -su hdfs ${HADOOP}/hadoop jar ${MR}/hadoop-examples.jar teragen \
	                     -Dmapreduce.job.maps=$i \
	                     -Dmapreduce.map.memory.mb=$k \
	                     -Dmapreduce.map.java.opts.max.heap=$MAP_MB \
	                     51200000 /results/tg-10GB-${i}-${j}-${k} 1>tera_${i}_${j}_${k}.out 2>tera_${i}_${j}_${k}.err
	
	        time sudo -su hdfs ${HADOOP}/hadoop jar $MR/hadoop-examples.jar terasort \
	                     -Dmapreduce.job.maps=$i \
	                     -Dmapreduce.job.reduces=$j \
	                     -Dmapreduce.map.memory.mb=$k \
	                     -Dmapreduce.map.java.opts.max.heap=$MAP_MB \
	                     -Dmapreduce.reduce.memory.mb=$k \
	                     -Dmapreduce.reduce.java.opts.max.heap=$RED_MB \
		             /results/tg-10GB-${i}-${j}-${k}  \
	                     /results/ts-10GB-${i}-${j}-${k} 1>>tera_${i}_${j}_${k}.out 2>>tera_${i}_${j}_${k}.err
	
	        sudo -su hdfs HADOOP/hadoop fs -rm -r -skipTrash /results/tg-10GB-${i}-${j}-${k}
	        sudo -su hdfs $HADOOP/hadoop fs -rm -r -skipTrash /results/ts-10GB-${i}-${j}-${k}
	      done
	   done
	done
	
	echo Testing loop ended on `date`


	[centos@ip-10-0-255-106 ~]$ ./YARNtest.sh
	Testing loop started on Wed Mar 22 16:02:43 UTC 2017
	/opt/cloudera/parcels/CDH/bin
	/opt/cloudera/parcels/CDH/bin
	
	real	1m8.386s
	user	0m7.146s
	sys	0m0.552s
	
	real	2m7.374s
	user	0m9.182s
	sys	0m0.652s
	/bin/bash: HADOOP/hadoop: Permission denied
	Deleted /results/ts-10GB-8-1-512
	/opt/cloudera/parcels/CDH/bin
	/opt/cloudera/parcels/CDH/bin
	
	real	1m3.674s
	user	0m7.191s
	sys	0m0.567s
	
	real	2m16.790s
	user	0m9.152s
	sys	0m0.668s
	/bin/bash: HADOOP/hadoop: Permission denied
	Deleted /results/ts-10GB-8-1-1024
	
	
# Fast Run

	#!/bin/sh
	# Confirm the path values given below correspond to your installation
	
	MR=/opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce
	HADOOP=/opt/cloudera/parcels/CDH/bin
	
	# Mark start of the loop
	echo Testing loop started on `date`
	
	# Mapper containers
	for i in 8
	do
	   # Reducer containers
	   for j in 2
	   do
	      # Container memory
	      for k in 512 1024
	      do
	         # Set mapper JVM heap
	         MAP_MB=`echo "($k*0.8)/1" | bc`
	
	         # Set reducer JVM heap
	         RED_MB=`echo "($k*0.8)/1" | bc`
		echo ${HADOOP}
		echo $HADOOP
	
	time sudo -su hdfs ${HADOOP}/hadoop jar ${MR}/hadoop-examples.jar teragen \
	                     -Dmapreduce.job.maps=$i \
	                     -Dmapreduce.map.memory.mb=$k \
	                     -Dmapreduce.map.java.opts.max.heap=$MAP_MB \
	                     51200000 /results/tg-10GB-${i}-${j}-${k} 1>tera_${i}_${j}_${k}.out 2>tera_${i}_${j}_${k}.err
	
	        time sudo -su hdfs ${HADOOP}/hadoop jar $MR/hadoop-examples.jar terasort \
	                     -Dmapreduce.job.maps=$i \
	                     -Dmapreduce.job.reduces=$j \
	                     -Dmapreduce.map.memory.mb=$k \
	                     -Dmapreduce.map.java.opts.max.heap=$MAP_MB \
	                     -Dmapreduce.reduce.memory.mb=$k \
	                     -Dmapreduce.reduce.java.opts.max.heap=$RED_MB \
		             /results/tg-10GB-${i}-${j}-${k}  \
	                     /results/ts-10GB-${i}-${j}-${k} 1>>tera_${i}_${j}_${k}.out 2>>tera_${i}_${j}_${k}.err
	
	        sudo -su hdfs HADOOP/hadoop fs -rm -r -skipTrash /results/tg-10GB-${i}-${j}-${k}
	        sudo -su hdfs $HADOOP/hadoop fs -rm -r -skipTrash /results/ts-10GB-${i}-${j}-${k}
	      done
	   done
	done
	
	echo Testing loop ended on `date`
	
	[centos@ip-10-0-255-106 ~]$ ./YARNtest.sh
	Testing loop started on Wed Mar 22 16:24:09 UTC 2017
	/opt/cloudera/parcels/CDH/bin
	/opt/cloudera/parcels/CDH/bin
	
	real	1m14.259s
	user	0m7.054s
	sys	0m0.582s
	
	real	1m59.181s
	user	0m9.474s
	sys	0m0.669s
	/bin/bash: HADOOP/hadoop: Permission denied
	Deleted /results/ts-10GB-8-2-512
	/opt/cloudera/parcels/CDH/bin
	/opt/cloudera/parcels/CDH/bin
	
	real	1m5.577s
	user	0m7.210s
	sys	0m0.571s
	
	real	2m6.001s
	user	0m9.092s
	sys	0m0.664s
	/bin/bash: HADOOP/hadoop: Permission denied
	Deleted /results/ts-10GB-8-2-1024
	Testing loop ended on Wed Mar 22 16:30:40 UTC 2017