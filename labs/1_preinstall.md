# 1. vm.swappiness
# cat /proc/sys/vm/swappiness
		30
# sudo sysctl vm.swappiness=1
# cat /proc/sys/vm/swappiness
		1

##############################

# 2. Show the mount attributes of your volume(s)
df -h

	Filesystem      Size  Used Avail Use% Mounted on
	/dev/xvda1      8.0G  876M  7.2G  11% /
	devtmpfs        3.6G     0  3.6G   0% /dev
	tmpfs           3.5G     0  3.5G   0% /dev/shm
	tmpfs           3.5G   17M  3.5G   1% /run
	tmpfs           3.5G     0  3.5G   0% /sys/fs/cgroup
	tmpfs           707M     0  707M   0% /run/user/1000
	tmpfs           707M     0  707M   0% /run/user/0


# lsblk


	NAME    MAJ:MIN RM SIZE RO TYPE MOUNTPOINT
	xvda    202:0    0   8G  0 disk
	└─xvda1 202:1    0   8G  0 part /
	xvdb    202:16   0  22G  0 disk

# sudo mkfs -t ext4 /dev/xvdb
# sudo -i
# mkdir -p /data/0
# chown `id -u` /data/0
# echo '/dev/xvdb /data/0 auto noatime,noexec,nodiratime 0 0' >> /etc/fstab
# mount -a /dev/xvdb /data/0


# cat /etc/fstab


	UUID=ef6ba050-6cdc-416a-9380-c14304d0d206 /                       xfs     	defaults        0 0
	/dev/xvdb /data/0 auto noatime,noexec,nodiratime 0 0

# df -h


	Filesystem      Size  Used Avail Use% Mounted on
	/dev/xvda1      8.0G  877M  7.2G  11% /
	devtmpfs        3.6G     0  3.6G   0% /dev
	tmpfs           3.5G     0  3.5G   0% /dev/shm
	tmpfs           3.5G   17M  3.5G   1% /run
	tmpfs           3.5G     0  3.5G   0% /sys/fs/cgroup
	tmpfs           707M     0  707M   0% /run/user/1000
	tmpfs           707M     0  707M   0% /run/user/0
	/dev/xvdb        22G   45M   21G   1% /data/0

###################################################

# 3. If you have ext-based volumes, list the reserve space setting


# tune2fs -l /dev/xvdb

	tune2fs 1.42.9 (28-Dec-2013)
		Filesystem volume name:   <none>
		Last mounted on:          <not available>
		Filesystem UUID:          998d9b72-f0d5-4ee8-a25f-d45ec914ff65
	Filesystem magic number:  0xEF53
	Filesystem revision #:    1 (dynamic)
	Filesystem features:      has_journal ext_attr resize_inode dir_index filetype needs_recovery extent 64bit flex_bg sparse_super large_file huge_file uninit_bg dir_nlink extra_isize
	Filesystem flags:         signed_directory_hash
	Default mount options:    user_xattr acl
	Filesystem state:         clean
	Errors behavior:          Continue
	Filesystem OS type:       Linux
	Inode count:              1441792
	Block count:              5767168
	Reserved block count:     288358
	Free blocks:              5632622
	Free inodes:              1441781
	First block:              0
	Block size:               4096
	Fragment size:            4096
	Group descriptor size:    64
	Reserved GDT blocks:      1024
	Blocks per group:         32768
	Fragments per group:      32768
	Inodes per group:         8192
	Inode blocks per group:   512
	Flex block group size:    16
	Filesystem created:       Mon Mar 20 19:26:57 2017
	Last mount time:          Mon Mar 20 19:31:40 2017
	Last write time:          Mon Mar 20 19:31:40 2017
	Mount count:              1
	Maximum mount count:      -1
	Last checked:             Mon Mar 20 19:26:57 2017
	Check interval:           0 (<none>)
	Lifetime writes:          132 MB
	Reserved blocks uid:      0 (user root)
	Reserved blocks gid:      0 (group root)
	First inode:              11
	Inode size:	          256
	Required extra isize:     28
	Desired extra isize:      28
	Journal inode:            8
	Default directory hash:   half_md4
	Directory Hash Seed:      df7f0962-1215-4cd0-bedc-534e3525a23e
	Journal backup:           inode blocks

##################################################
#4. Disable transparent hugepage support

	cat /sys/kernel/mm/transparent_hugepage/enabled
	[always] madvise never
	[root@ip-10-0-10-122 ~]# cat /sys/kernel/mm/transparent_hugepage/defrag
	[always] madvise never
	
	echo never > /sys/kernel/mm/transparent_hugepage/enabled
	[root@ip-10-0-10-122 ~]# cat /sys/kernel/mm/transparent_hugepage/enabled
	always madvise [never]
	
	echo never > /sys/kernel/mm/transparent_hugepage/defrag
	[root@ip-10-0-10-122 ~]# cat /sys/kernel/mm/transparent_hugepage/defrag
	always madvise [never]

########################################################

#5. List your network interface configuration

	[root@ip-10-0-10-106 ~]# ifconfig -a
	eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001
	        inet 10.0.10.106  netmask 255.255.255.0  broadcast 10.0.10.255
	        inet6 fe80::49:faff:fe88:a6d9  prefixlen 64  scopeid 0x20<link>
	        ether 02:49:fa:88:a6:d9  txqueuelen 1000  (Ethernet)
	        RX packets 1523  bytes 126468 (123.5 KiB)
	        RX errors 0  dropped 0  overruns 0  frame 0
	        TX packets 1267  bytes 151228 (147.6 KiB)
	        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
	
	lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
	        inet 127.0.0.1  netmask 255.0.0.0
	        inet6 ::1  prefixlen 128  scopeid 0x10<host>
	        loop  txqueuelen 0  (Local Loopback)
	        RX packets 70  bytes 5984 (5.8 KiB)
	        RX errors 0  dropped 0  overruns 0  frame 0
	        TX packets 70  bytes 5984 (5.8 KiB)
	        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
# ##################################################

# 6. Show correct forward and reverse host lookups

# yum install bind-utils

	[root@ip-10-0-10-106 ~]# nslookup 10.0.10.106
	Server:		10.0.0.2
	Address:	10.0.0.2#53
	
	Non-authoritative answer:
	106.10.0.10.in-addr.arpa	name = ip-10-0-10-106.us-west-2.compute.internal.
	
	Authoritative answers can be found from:
	
	[root@ip-10-0-10-106 ~]# nslookup ip-10-0-10-106.us-west-2.compute.internal
	Server:		10.0.0.2
	Address:	10.0.0.2#53
	
	Non-authoritative answer:
	Name:	ip-10-0-10-106.us-west-2.compute.internal
	Address: 10.0.10.106

# #############################################

#7. Show the nscd service is running

	yum install nscd
	chkconfig --level 345 nscd on
	service nscd start
	verify using nscd -g
	
	[root@ip-10-0-10-106 ~]# nscd -g
	nscd configuration:
	
	              0  server debug level
	            25s  server runtime
	              5  current number of threads
	             32  maximum number of threads
	              0  number of times clients had to wait
	             no  paranoia mode enabled
	           3600  restart internal
	              5  reload count
	
	passwd cache:
	
	            yes  cache is enabled
	            yes  cache is persistent
	            yes  cache is shared
	            211  suggested size
	         216064  total data pool size
	              0  used data pool size
	            600  seconds time to live for positive entries
	             20  seconds time to live for negative entries
	              0  cache hits on positive entries
	              0  cache hits on negative entries
	              0  cache misses on positive entries
	              0  cache misses on negative entries
	              0% cache hit rate
	              0  current number of cached values
	              0  maximum number of cached values
	              0  maximum chain length searched
	              0  number of delays on rdlock
	              0  number of delays on wrlock
	              0  memory allocations failed
	            yes  check /etc/passwd for changes
	
	group cache:
	
	            yes  cache is enabled
	            yes  cache is persistent
	            yes  cache is shared
	            211  suggested size
	         216064  total data pool size
	              0  used data pool size
	           3600  seconds time to live for positive entries
	             60  seconds time to live for negative entries
	              0  cache hits on positive entries
	              0  cache hits on negative entries
	              0  cache misses on positive entries
	              0  cache misses on negative entries
	              0% cache hit rate
	              0  current number of cached values
	              0  maximum number of cached values
	              0  maximum chain length searched
	              0  number of delays on rdlock
	              0  number of delays on wrlock
	              0  memory allocations failed
	            yes  check /etc/group for changes
	
	hosts cache:
	
	            yes  cache is enabled
	            yes  cache is persistent
	            yes  cache is shared
	            211  suggested size
	         216064  total data pool size
	              0  used data pool size
	           3600  seconds time to live for positive entries
	             20  seconds time to live for negative entries
	              0  cache hits on positive entries
	              0  cache hits on negative entries
	              0  cache misses on positive entries
	              0  cache misses on negative entries
	              0% cache hit rate
	              0  current number of cached values
	              0  maximum number of cached values
	              0  maximum chain length searched
	              0  number of delays on rdlock
	              0  number of delays on wrlock
	              0  memory allocations failed
	            yes  check /etc/hosts for changes
	
	services cache:
	
	            yes  cache is enabled
	            yes  cache is persistent
	            yes  cache is shared
	            211  suggested size
	         216064  total data pool size
	              0  used data pool size
	          28800  seconds time to live for positive entries
	             20  seconds time to live for negative entries
	              0  cache hits on positive entries
	              0  cache hits on negative entries
	              0  cache misses on positive entries
	              0  cache misses on negative entries
	              0% cache hit rate
	              0  current number of cached values
	              0  maximum number of cached values
	              0  maximum chain length searched
	              0  number of delays on rdlock
	              0  number of delays on wrlock
	              0  memory allocations failed
	            yes  check /etc/services for changes
	
	netgroup cache:
	
	            yes  cache is enabled
	            yes  cache is persistent
	            yes  cache is shared
	            211  suggested size
	         216064  total data pool size
	              0  used data pool size
	          28800  seconds time to live for positive entries
	             20  seconds time to live for negative entries
	              0  cache hits on positive entries
	              0  cache hits on negative entries
	              0  cache misses on positive entries
	              0  cache misses on negative entries
	              0% cache hit rate
	              0  current number of cached values
	              0  maximum number of cached values
	              0  maximum chain length searched
	              0  number of delays on rdlock
	              0  number of delays on wrlock
	              0  memory allocations failed
	            yes  check /etc/netgroup for changes
	
	SELinux AVC Statistics:
	
	              1  entry lookups
	              0  entry hits
	              1  entry misses
	              0  entry discards
	              1  CAV lookups
	              0  CAV hits
	              0  CAV probes
	              1  CAV misses

# ########################################

#8. Show the ntpd service is running

	 yum install ntp ntpdate ntp-doc
	 chkconfig ntpd on
	 ntpdate pool.ntp.org
	 service ntpd start
	
	[root@ip-10-0-10-106 ~]# service ntpd status
	Redirecting to /bin/systemctl status  ntpd.service
	● ntpd.service - Network Time Service
	   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; enabled; vendor preset: disabled)
	   Active: active (running) since Mon 2017-03-20 20:53:46 UTC; 1min 4s ago
	  Process: 16552 ExecStart=/usr/sbin/ntpd -u ntp:ntp $OPTIONS (code=exited, status=0/SUCCESS)
	 Main PID: 16553 (ntpd)
	   CGroup: /system.slice/ntpd.service
	           └─16553 /usr/sbin/ntpd -u ntp:ntp -g
	
	Mar 20 20:53:46 ip-10-0-10-106 ntpd[16553]: Listen normally on 2 lo 127.0.0.1...3
	Mar 20 20:53:46 ip-10-0-10-106 ntpd[16553]: Listen normally on 3 eth0 10.0.10...3
	Mar 20 20:53:46 ip-10-0-10-106 ntpd[16553]: Listen normally on 4 lo ::1 UDP 123
	Mar 20 20:53:46 ip-10-0-10-106 ntpd[16553]: Listen normally on 5 eth0 fe80::4...3
	Mar 20 20:53:46 ip-10-0-10-106 ntpd[16553]: Listening on routing socket on fd...s
	Mar 20 20:53:46 ip-10-0-10-106 systemd[1]: Started Network Time Service.
	Mar 20 20:53:47 ip-10-0-10-106 ntpd[16553]: 0.0.0.0 c016 06 restart
	Mar 20 20:53:47 ip-10-0-10-106 ntpd[16553]: 0.0.0.0 c012 02 freq_set kernel 0...M
	Mar 20 20:53:47 ip-10-0-10-106 ntpd[16553]: 0.0.0.0 c011 01 freq_not_set
	Mar 20 20:53:53 ip-10-0-10-106 ntpd[16553]: 0.0.0.0 c614 04 freq_mode
	Hint: Some lines were ellipsized, use -l to show in full.

# #############################################















































