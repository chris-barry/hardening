# Windows 7
* How to change Admin passwords.
  * From the Start menu, select Control Panel. If you are not already in Category View, in the upper left, click Category   View. Then, click User Accounts and Family Safety.
  * Under "User Accounts", click Change your Windows password. If prompted, click Continue.
  * Under "Make changes to your user account", click Set a password.
  * In the "New password" and "Confirm new password" fields, enter the password. Click OK twice.
* Check running services.
  * From a command prompt: Start | Run (type) cmd (click Ok)
  * (type) tasklist /svc (press Enter) 
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
  * (press) `win -r` (type) `msconfig.msc`
  * (click) the Startup tab
