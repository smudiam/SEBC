#Error Syncing hue user accounts with Linux
	
	[root@ip-10-0-255-106 ~]# cd /opt/cloudera/parcels/CDH/lib/hue/
	[root@ip-10-0-255-106 hue]# ls
	app.reg  build     desktop  LICENSE.txt  Makefile.buildvars  Makefile.vars       NOTICE.txt  tools
	apps     cloudera  ext      Makefile     Makefile.sdk        Makefile.vars.priv  README      VERSION
	[root@ip-10-0-255-106 hue]# build/env/bin/hue useradmin_sync_with_unix
	Error: Password not present
	Traceback (most recent call last):
	  File "build/env/bin/hue", line 12, in <module>
	    load_entry_point('desktop==3.9.0', 'console_scripts', 'hue')()
	  File "/opt/cloudera/parcels/CDH-5.10.0-1.cdh5.10.0.p0.41/lib/hue/desktop/core/src/desktop/manage_entry.py", line 59, in entry
	    execute_from_command_line(sys.argv)
	  File "/opt/cloudera/parcels/CDH-5.10.0-1.cdh5.10.0.p0.41/lib/hue/build/env/lib/python2.7/site-packages/Django-1.6.10-py2.7.egg/django/core/management/__init__.py", line 399, in execute_from_command_line
	    utility.execute()
	  File "/opt/cloudera/parcels/CDH-5.10.0-1.cdh5.10.0.p0.41/lib/hue/build/env/lib/python2.7/site-packages/Django-1.6.10-py2.7.egg/django/core/management/__init__.py", line 392, in execute
	    self.fetch_command(subcommand).run_from_argv(self.argv)
	  File "/opt/cloudera/parcels/CDH-5.10.0-1.cdh5.10.0.p0.41/lib/hue/build/env/lib/python2.7/site-packages/Django-1.6.10-py2.7.egg/django/core/management/__init__.py", line 261, in fetch_command
	    commands = get_commands()
	  File "/opt/cloudera/parcels/CDH-5.10.0-1.cdh5.10.0.p0.41/lib/hue/build/env/lib/python2.7/site-packages/Django-1.6.10-py2.7.egg/django/core/management/__init__.py", line 107, in get_commands
	    apps = settings.INSTALLED_APPS
	  File "/opt/cloudera/parcels/CDH-5.10.0-1.cdh5.10.0.p0.41/lib/hue/build/env/lib/python2.7/site-packages/Django-1.6.10-py2.7.egg/django/conf/__init__.py", line 54, in __getattr__
	    self._setup(name)
	  File "/opt/cloudera/parcels/CDH-5.10.0-1.cdh5.10.0.p0.41/lib/hue/build/env/lib/python2.7/site-packages/Django-1.6.10-py2.7.egg/django/conf/__init__.py", line 49, in _setup
	    self._wrapped = Settings(settings_module)
	  File "/opt/cloudera/parcels/CDH-5.10.0-1.cdh5.10.0.p0.41/lib/hue/build/env/lib/python2.7/site-packages/Django-1.6.10-py2.7.egg/django/conf/__init__.py", line 128, in __init__
	    mod = importlib.import_module(self.SETTINGS_MODULE)
	  File "/opt/cloudera/parcels/CDH-5.10.0-1.cdh5.10.0.p0.41/lib/hue/build/env/lib/python2.7/site-packages/Django-1.6.10-py2.7.egg/django/utils/importlib.py", line 40, in import_module
	    __import__(name)
	  File "/opt/cloudera/parcels/CDH-5.10.0-1.cdh5.10.0.p0.41/lib/hue/desktop/core/src/desktop/settings.py", line 323, in <module>
	    "PASSWORD" : desktop.conf.get_database_password(),
	  File "/opt/cloudera/parcels/CDH-5.10.0-1.cdh5.10.0.p0.41/lib/hue/desktop/core/src/desktop/conf.py", line 1408, in get_database_password
	    password = DATABASE.PASSWORD_SCRIPT.get()
	  File "/opt/cloudera/parcels/CDH-5.10.0-1.cdh5.10.0.p0.41/lib/hue/desktop/core/src/desktop/lib/conf.py", line 147, in get
	    return self.config.get_value(data, present=present, prefix=self.prefix, coerce_type=True)
	  File "/opt/cloudera/parcels/CDH-5.10.0-1.cdh5.10.0.p0.41/lib/hue/desktop/core/src/desktop/lib/conf.py", line 263, in get_value
	    return self._coerce_type(raw_val, prefix)
	  File "/opt/cloudera/parcels/CDH-5.10.0-1.cdh5.10.0.p0.41/lib/hue/desktop/core/src/desktop/lib/conf.py", line 283, in _coerce_type
	    return self.type(raw)
	  File "/opt/cloudera/parcels/CDH-5.10.0-1.cdh5.10.0.p0.41/lib/hue/desktop/core/src/desktop/lib/conf.py", line 714, in coerce_password_from_script
	    raise subprocess.CalledProcessError(p.returncode, script)
	subprocess.CalledProcessError: Command '/run/cloudera-scm-agent/process/303-hue-HUE_SERVER/altscript.sh sec-5-password' returned non-zero exit status 1
	[root@ip-10-0-255-106 hue]# packet_write_wait: Connection to 34.208.28.66 port 22: Broken pipe
	Satyas-MacBook-Pro:~ satya$
