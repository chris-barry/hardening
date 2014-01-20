# CentOS

* How to change root passwords.
	* `su root; passwd;`
* Check running services.
	* `top`
	* For a better experience, install `htop`
* Check open network connections.
	* Open connections with application name: `lsof -i -nP`
	* All TCP connections: `lsof -i TCP`
	* What a user is running: `lsof -u [username]`
* How to delete a user account.
	* `userdel [username]`
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

## TODO
* How to configure firewall.
* How to stop unused services.
