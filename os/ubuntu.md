# Ubuntu
* How to change root passwords.
	* `su root; passwd;`
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
	* If you aren't on the sudoers list, you have to run as root.
* Install program from repository.
	* `apt-get install [program name]`
* Remove program from repository.
	* `apt-get remove [program name]`
* Update system
	* `apt-get update; apt-get upgrade;`
* Stopping services:
	* `pkill [program]`.
	* Check `top` or `htop` for what is running.

## TODO
* How to configure firewall.
* Some backup repositories (\*nix only).
* Check what runs at startup.
	* Look in `/etc/rc*.d/`.
	* This is where you will see what runs at startup.
