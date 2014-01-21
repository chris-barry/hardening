# CentOS

* How to change root passwords.
	* `su root; passwd;`
* Check running services.
	* `ps aux` -- greppable list
	* `top`
	* For a better experience, install `htop`
	* `lsof -p [pid]` -- investigate specific PID
* Check services with runlevel info (pre-systemd systems)
	* `chkconfig --list`
* Start service.
	* `service [servicename] start`
* Stop service.
	* `service [servicename] stop`
* Restart service.
	* `service [servicename] restart`
* Check open network connections.
	* Open connections with application name: `lsof -i -nP`
	* All TCP connections: `lsof -i TCP`
	* What a user is running: `lsof -u [username]`
* How to delete a user account.
	* `userdel [username]`
* Query installed packages
	* `rpm -qa`
* Verify packages
	* `rpm -Va`
* Install program from repository.
	* `yum install [program name]`
* Remove program from repository.
	* `yum remove [program name]`
* Update system
	* `yum update` -- refreshes repos, then updates packages
* Some backup repositories (\*nix only).
	* Manually: <https://www.centos.org/download/mirrors/>
	* `yum install yum-fastestmirror`
	* Edit: `/etc/yum/pluginconf.d/fastestmirror.conf`
	```
	[main]
	verbose = 0
	socket_timeout = 3
	enabled = 1
	hostfilepath = /var/cache/yum/timedhosts.txt
	maxhostfileage = 1
	```
* Check what runs at startup.
	* `/usr/sbin/ntsysv`
* 
	* `netstat -nap`
* Check for cronjobs scheduled by root
	* `crontab -u root -l`
* Check for cronjobs
	* `cat /etc/crontab`
	 * `ls /etc/cron.*`
 
## TODO
* How to configure firewall.
* How to stop unused services.
