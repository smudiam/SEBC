

# Teragen

	real	2m0.934s
	user	0m7.477s
	sys	0m0.593s
	
	-Dmapreduce.job.maps=8
	-Dmapreduce.map.memory.mb=256
	-Dmapreduce.map.java.opts.max.heap=204
	
	real	2m5.481s
	user	0m7.498s
	sys	0m0.593s
	
	
	-Dmapreduce.job.maps=8
	-Dmapreduce.map.memory.mb=1024
	-Dmapreduce.map.java.opts.max.heap=819



# Terasort

	real	0m40.089s
	user	0m8.682s
	sys	0m0.665s
	
	-Dmapreduce.job.maps=8
	-Dmapreduce.job.reduces=2
	-Dmapreduce.map.memory.mb=256
	-Dmapreduce.map.java.opts.max.heap=204
	-Dmapreduce.reduce.memory.mb=256
	-Dmapreduce.reduce.java.opts.max.heap=204
	
	real	3m49.322s
	user	0m9.390s
	sys	0m0.751s
	
	-Dmapreduce.job.maps=8
	-Dmapreduce.job.reduces=2
	-Dmapreduce.map.memory.mb=1024
	-Dmapreduce.map.java.opts.max.heap=819
	-Dmapreduce.reduce.memory.mb=1024
	-Dmapreduce.reduce.java.opts.max.heap=819




	
