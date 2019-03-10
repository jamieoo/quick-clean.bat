# quick-clean.bat
::Summary:
	::this is a script for quickly freeing disk space on multiple remote PC's. 
	::the script starts PsExec64.exe, which in turn starts cleanmgr.exe on any machine that you specify in the script (by machine name or IP).
	::this   


::Setup:
	::0. login directly with SA account
	::1. download PsTools: https://download.sysinternals.com/files/PSTools.zip
	::2. extract PSTools.zip to C:/Windows/System32.
	::3. paste script in text editor. Edit bracketed sections with your info.
	::4. run the script in CMD/powershell, alternatively you can save this as a .bat file to your desktop. 

::Notes:
	::cleanmgr.exe will run silently, but always contact machine owners prior to running this script.  
	::/verylow flag disk removes: downloaded program files, temp internet files, offline webpages, recycle bin, setup log files, temp files, thumbnails.
	::brackets denote user entry- do not include in script.

::Future Updates:
	::script will return a text file of all supplied offline/unreachable machines(1). 
	::script will be scheduled to start automatically the next time a user logins to a machine(1). 



