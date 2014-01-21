# Windows 7
* How to change Admin passwords.
  * From the Start menu, select Control Panel. If you are not already in Category View, in the upper left, click Category   View. Then, click User Accounts and Family Safety.
  * Under "User Accounts", click Change your Windows password. If prompted, click Continue.
  * Under "Make changes to your user account", click Set a password.
  * In the "New password" and "Confirm new password" fields, enter the password. Click OK twice.
* Check running services.
  * From a command prompt: Start | Run (type) cmd (click Ok)
  * `tasklist /svc` 
  * or `wmic process list full`
  * Or in the GUI: `services.msc`
* To Remove any unneeded running Processes
  * Log on as Administrator
  * Start | Settings | Control Panel | Administrative Tools | Services
* Check open network connections.
  * From a Command Prompt (type) `netstat -ano`
* How do delete an account.
  * (press) `win -r` then (type) `lusrmgr.msc`
  * (click) Users folder in the left pane to open it.
  * Right click on the user account that you want to delete, and click on Delete.
  * (click) yes
* Delete a User Account on a Domain
  * In the elevated command prompt, type the command below, and press Enter. 
  * `net user "UserName" /delete`
  * In Windows Explorer, navigate to this user account's `C:\Users\(user-name)` profile folder (ex: Example-Standard), right click or press and hold on it, click on Delete, and approve. 
* Check what runs at startup.
  * `schtasks`
  * `wmic startup list full`
  * (press) `win -r` (type) `msconfig.msc`
  * (click) the Startup tab
* Turn UAC(User Account Control) to the max.
  * Control Panel\All Control Panel Items\User Accounts\Change User Account Control Settings Move slider to top
* Set up Firewall Profile
  * Control Panel | Network and Sharing Center
  * Change network location to `Public`.
* Use only Bare Essential Network protocols.
  * Control Panel | Network and Sharing Center Local Area Connection | Properties button 
  * Uncheckmark the following:
    * Client for MS Networks
    * File and Printer Sharing for Microsoft Networks (CAREFULL!!)
    * QoS
    * Link Layer Topology Discovery Mapper IO Driver
    * Link Layer Topology Discovery Responder
    * Internet protocol version 6
  * Select 'Internet Protocol version 4 (TCP IPv4), click Properties, (click) Advanced,
    * Click 'DNS' tab, uncheck 'register this connections address in DNS'
    * Click 'WINS' tab, select 'Disable NETBIOS over TCP/IP'
* Disable IPV6 Totally
 * (press) `win -r` (type) ` regedit.exe`
    * HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Tcpip6\Parameters \ 
    * Double-click DisabledComponents to change the DisabledComponents entry.
* Disable unused tcpip6 Devices and NETBT
  * Control Panel | Device Manager, View menu |Show Hidden Devices
  * /Network, disable Wan Miniport IPv6
  * /Network, disable Microsoft ISATAP adapter (IPv6 tunnel)
  * /Network, disable Teredo Tunneling Pseudo Interface (IPv6 tunnel)
  * /Non-Plug and Play Drivers /Remote Access IPv6 ARP Driver > Properties > Driver tab >: Change Startup Type from System to Disable
  *  /Non-Plug and Play Drivers / NETBT > Properties > Driver tab > Stop it and change Type from 'System' to 'Disabled'. (disables NETBIOS totally. partially closes port 445)

* Logs
  * GUI: `eventvrw.msc`

TODO: 

* Add more about wmic
