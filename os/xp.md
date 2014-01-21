# Windows XP
##Change Admin Password
1. From the Start menu, select Control Panel, or Settings and then Control Panel. Double-click the User Accounts icon.
2. From the Users tab, click the name of the administrative account, and then click Reset Password... .
3. In the "New password" and "Confirm new password" fields, enter the password. Click OK twice. 

## Stop storing LANMAN hashes
Pre-Vista Windows computers still store LANMAN Hashes of passwords. It's best to disable this.
http://support.microsoft.com/kb/299656
* `HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\LSA`
  * Add a new key `NoLMHash`, click `OK`.

## Stop sending LANMAN across network
It's also a good idea to disable LANMAN authentication across the network. 
* `HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\LSA\LMCompatibilityLevel` -- choose a value from here: http://technet.microsoft.com/en-us/library/cc960646.aspx
