# Debian
* How to change root passwords.
	* `su root; passwd;`
* Some backup repositories (\*nix only).
	* Automated: `netselect` will determine the fastest for you.
	* Else, <ftp://ftp.us.debian.org/debian/>
* Check running services.
	* `top`
	* For a better experience, install `htop`
* Check open network connections.
	* Open connections with application name: `lsof -i -nP`
	* All TCP connections: `lsof -i TCP`
	* What a user is running: `lsof -u [username]`
* How do delete an account.
	* `userdel [username]`
* Check cron (for all users).
	* `crontab -e`
* Check sudoers file
	* `visudo`
* Install program from repository.
	* `apt-get install [program name]`
* Remove program from repository.
	* `apt-get remove [program name]`

## TODO
* How to configure firewall.
* How to stop unused services.
* Check what runs at startup.
