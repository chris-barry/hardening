# FTP
* Install vsftpd on your virtual private server 
  * `sudo yum install vsftpd`
* Install the FTP client
  * sudo `yum install ftp`
* Open up the configuration file:
  * `sudo vi /etc/vsftpd/vsftpd.conf`
* Change you need to make is to change the Anonymous_enable to No:
  * anonymous_enable=NO
  * local_enable=YES
  * chroot_local_user=YES
* Finish up by restarting vsftpd
  * `sudo service vsftpd restart`
* ensure that vsftpd runs at boot, run chkconfig:
  * chkconfig vsftpd on
* Check this - You can disable the login ssh with and just for ftp:
  * `usermod -s /sbin/nologin userftp`
* Disable shell access to ftp user:
  * Edit the file /etc/shells and add the line /bin/false:
  `echo "/bin/false" >> /etc/shells`
* I don't give access to port 20 so turn this off
  * connect_from_port_20=NO
* SSL 
  * ssl_enable=yes
  * force_local_data_ssl=yes
  * force_local_logins_ssl=yes
* You can also restrict the commands that user can give. For example if you want only to upload/download files, and don't let people to delete files add this line:
  * cmds_allowed=PASV,BINARY,PUT,GET,PWD,STAT,TYPE,NLST,CWD,SIZE,MDTM,SITE,UTIME,REST,RETR,STOR,LIST,ASCII,RETR,QUIT
* Changing vsftp port
  * listen_port=21
     
## Example Config.
*Create an SSL certificate if you don't already have one:

`openssl req -x509 -nodes -days 365 -newkey rsa:1024 -keyout /etc/vsftpd/vsftpd.pem -out /etc/vsftpd/vsftpd.pem`

* anonymous_enable=NO
* local_enable=YES
* write_enable=YES
* local_umask=022
* dirmessage_enable=YES
* xferlog_enable=YES
* connect_from_port_20=YES
* xferlog_std_format=YES
* ftpd_banner=Welcome to blah FTP service.
* listen=YES

* pam_service_name=vsftpd
* userlist_enable=YES
* tcp_wrappers=YES

* pasv_enable=YES
* pasv_promiscuous=YES
* pasv_min_port=6000
* pasv_max_port=7000

* ssl_enable=YES
* allow_anon_ssl=NO
* force_local_logins_ssl=YES
* ssl_tlsv1=YES
* ssl_sslv2=YES
* ssl_sslv3=YES
* rsa_cert_file=/etc/vsftpd/vsftpd.pem
* rsa_private_key_file=/etc/vsftpd/vsftpd.pem

