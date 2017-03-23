# krb5.conf

	[root@ip-10-0-255-106 krb5kdc]# cat /etc/krb5.conf
	# Configuration snippets may be placed in this directory as well
	includedir /etc/krb5.conf.d/
	
	[logging]
	 default = FILE:/var/log/krb5libs.log
	 kdc = FILE:/var/log/krb5kdc.log
	 admin_server = FILE:/var/log/kadmind.log
	
	
	[libdefaults]
	 default_realm = SMUDIAM.COM
	 dns_lookup_realm = false
	 dns_lookup_kdc = false
	 ticket_lifetime = 24h
	 renew_lifetime = 7d
	 forwardable = true
	 udp_preference_limit = 1
	# default_ccache_name = KEYRING:persistent:%{uid}
	 default_tgs_enctypes = arcfour-hmac
	 default_tkt_enctypes = arcfour-hmac
	
	[realms]
	  SMUDIAM.COM = {
	  kdc = ip-10-0-255-106.us-west-2.compute.internal:88
	  admin_server = ip-10-0-255-106.us-west-2.compute.internal:749
	 }

	[domain_realm]
	   .example.com = SMUDIAM.COM
	   example.com = SMUDIAM.COM