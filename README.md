# quick-clean.bat
::Summary:
	::this is a script for quickly freeing disk space on multiple remote PC's. 
	::the script starts PsExec64.exe, which in turn starts cleanmgr.exe on any machine that you specify in the script (by machine name or IP).
	::this   


::Setup:
	::0. login directly to your machine with SA account
	::1. download PsTools: https://download.sysinternals.com/files/PSTools.zip
	::2. extract PSTools.zip to C:/Windows/System32.
	::3. paste script in text editor. Edit bracketed sections with your info.
	::4. run the script in CMD/powershell, alternatively you can save this as a .bat file to your desktop. 

::Notes:
	::cleanmgr.exe will run silently, but always contact machine owners prior to running this script.  
	::/verylow flag disk removes: downloaded program files, temp internet files, offline webpages, recycle bin, setup log files, temp files, thumbnails.
	::brackets denote user entry- do not include in script.

::Future-Updates:
	::replace >psexec with >pssession. 
	::return qc-offline of all offline/unreachable machines.
	::script will be scheduled to start again automatically the next time the deployed-to user logins with their credentials to a machnine found in qc-offline(>Register-ScheduledJob). 



