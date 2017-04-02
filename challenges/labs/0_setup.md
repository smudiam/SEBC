# Indicate the cloud provider you are using (AWS, GCE, Azure, other)
	AWS - US-West-2

# List the nodes you are using by IP address and private DNS name
	Private IPs:
	52.33.56.35
	34.208.107.167
	34.208.236.75
	35.163.102.117
	52.34.236.102

	
	internal:
	10.0.255.164,10.0.255.18,10.0.255.220,10.0.255.194,10.0.255.217


	Private DNS:
	ip-10-0-255-164.us-west-2.compute.internal
	ip-10-0-255-18.us-west-2.compute.internal
	ip-10-0-255-220.us-west-2.compute.internal
	ip-10-0-255-194.us-west-2.compute.internal
	ip-10-0-255-217.us-west-2.compute.internal
	
	
# Show the command and output that lists the Linux release you are using
	cat /etc/centos-release
	root@ip-10-0-255-164 ~]# cat /etc/centos-release
	CentOS Linux release 7.3.1611 (Core)
	


# Show the disk capacity available on each node is >= 30 GB
	lsbk
	[root@ip-10-0-255-164 ~]# lsblk
	NAME    MAJ:MIN RM SIZE RO TYPE MOUNTPOINT
	xvda    202:0    0  30G  0 disk
	└─xvda1 202:1    0  30G  0 part /
	xvdb    202:16   0  30G  0 disk /data/0
	
# Give the command and output for the contents of /etc/yum.repos.d/

	ls -al /etc/yum.repos.d/
	[root@ip-10-0-255-164 ~]# ls -al /etc/yum.repos.d
	total 52
	drwxr-xr-x.  2 root root 4096 Mar 24 15:23 .
	drwxr-xr-x. 80 root root 8192 Mar 24 15:19 ..
	-rw-r--r--.  1 root root 1664 Nov 29 18:12 CentOS-Base.repo
	-rw-r--r--.  1 root root 1309 Nov 29 18:12 CentOS-CR.repo
	-rw-r--r--.  1 root root  649 Nov 29 18:12 CentOS-Debuginfo.repo
	-rw-r--r--.  1 root root  314 Nov 29 18:12 CentOS-fasttrack.repo
	-rw-r--r--.  1 root root  630 Nov 29 18:12 CentOS-Media.repo
	-rw-r--r--.  1 root root 1331 Nov 29 18:12 CentOS-Sources.repo
	-rw-r--r--.  1 root root 2893 Nov 29 18:12 CentOS-Vault.repo
	
## These were not to be installed as part of the platform
	-rw-r--r--   1 root root 1416 Sep 12  2016 mysql-community.repo
	-rw-r--r--   1 root root 1440 Sep 12  2016 mysql-community-source.repo
	
# List the /etc/passwd entries for berkeley and stanford

	[root@ip-10-0-255-164 ~]# cat /etc/passwd | grep 'berkeley\|stanford'
	berkeley:x:2040:2422::/home/berkeley:/bin/bash
	stanford:x:2420:2421::/home/stanford:/bin/bash

# List the /etc/group entries for cardinal and bruins
	[root@ip-10-0-255-164 ~]# cat /etc/group | grep 'bruins\|cardinal'
	cardinal:x:2421:
	bruins:x:2422:
		
