
# List the command and output for ls /etc/yum.repos.d
	[root@ip-10-0-255-18 log]# ls -al
	total 420
	drwxr-xr-x.  8 root   root     4096 Mar 24 15:19 .
	drwxr-xr-x. 19 root   root     4096 Mar 24 15:19 ..
	drwxr-xr-x.  2 root   root        6 Feb 22  2016 anaconda
	drwx------.  2 root   root       22 Mar  3 03:42 audit
	-rw-r--r--.  1 root   root      183 Mar 24 15:19 boot.log
	-rw-------.  1 root   utmp    12672 Mar 24 16:21 btmp
	drwxr-xr-x.  2 chrony chrony      6 Dec  6 22:42 chrony
	-rw-r--r--.  1 root   root     4735 Mar 24 15:19 cloud-init.log
	-rw-r--r--.  1 root   root     3196 Mar 24 15:19 cloud-init-output.log
	-rw-r--r--.  1 root   root     4692 Mar 24 16:01 cron
	-rw-r--r--   1 root   root    32327 Mar 24 15:19 dmesg
	-rw-r--r--.  1 root   root    35637 Mar 24 13:59 dmesg.old
	-rw-------.  1 root   root     1941 Mar 24 15:06 grubby
	-rw-r--r--.  1 root   root   706932 Mar 24 16:12 lastlog
	-rw-------.  1 root   root      406 Mar 24 15:19 maillog
	-rw-------.  1 root   root   214374 Mar 24 16:37 messages
	drwxr-xr-x.  2 ntp    ntp         6 Feb  6 07:34 ntpstats
	drwx------.  2 root   root        6 Jun 10  2014 ppp
	-rw-------.  1 root   root    21767 Mar 24 16:44 secure
	-rw-------.  1 root   root        0 Feb 22  2016 spooler
	-rw-------.  1 root   root        0 Feb 22  2016 tallylog
	drwxr-xr-x.  2 root   root       22 Dec  6 22:26 tuned
	-rw-rw-r--.  1 root   utmp     7680 Mar 24 16:04 wtmp
	-rw-------.  1 root   root    12665 Mar 24 16:25 yum.log
	
# Use the scm_prepare_database.sh script to write your db.properties file
	/usr/share/cmf/schema/scm_prepare_database.sh -h ip-10-0-255-164.us-west-2.compute.internal -u root -p  --scm-host `hostname -f` mysql scm scm