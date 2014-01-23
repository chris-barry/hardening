Check if running legacy DFS or DFSR
* If possible, upgrade. http://technet.microsoft.com/en-us/library/cc773238(WS.10).aspx#BKMK_026
* If can't upgrade.
  * Background
    * http://redmondmag.com/articles/2011/02/01/dfs-best-practices.aspx 
    * http://technet.microsoft.com/en-us/library/cc782417.aspx
    * http://technet.microsoft.com/en-us/magazine/gg690154.aspx
  * Weep
  
Install Updates
* Get R2 installed
* Specific Hotfixes: http://blogs.technet.com/b/instan/archive/2012/06/03/cheat-sheet-for-dfs-n-and-dfs-r-on-windows-2008-r2-and-windows-7.aspx

Configure Namespaces
* c:/ shouldn't be shared
* TODO - IPS$ share?
 
Check running services
Check Scheduled Tasks
Check permissions

Run Best Practice Analyzer once R2 is installed
* http://technet.microsoft.com/en-us/library/dd759260.aspx
* http://technet.microsoft.com/en-us/library/dd759206.aspx

Background I don't have coherent bulleted steps for:
* Best Practices Guide, legacy and 2008
  * http://blogs.technet.com/b/josebda/archive/2009/03/10/the-basics-of-the-windows-server-2008-distributed-file-system-dfs.aspx
*Setup Guide, 2008
  * http://technet.microsoft.com/en-us/library/cc732863(v=ws.10).aspx
  
TO DO
* Steps for changing replication groups and root
