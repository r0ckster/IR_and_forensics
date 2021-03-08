## Get hostname, version, domain, hw-info, hotfixes...
* `>systeminfo`

## Last logons
1. Check useraccounts `>net user`
2. Search last logon for specific user `>net user <username> </domain> | findstr /B /C:"Last logon"`

## Check whats running at boot
* Use Task Manager `Task Manager > Startup`
* Or Regedit `HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\Run (OR RunOnce)`

## Check admin/user rights
* in cmd for a specific user `>net user <user>` and see "Group Memberships"
* from GUI: `Computer Management > Local Users and Groups` 

## Check scheduled tasks
* from cmd `>schtasks` or more specified `>schtasks /query /v`
* from GUI `Computer Management > System tools > Task Scheduler`

## Check hosts file for DNS poisoning for example
* Location: `C:\Windows\System32\drivers\etc\hosts`

## Check Firewall inbound/outbound rules
* Windows Firewall with Advanced Security
* If logging is on, check file `C:\Windows\system32\LogFiles\Firewall\pfirewall.log`

## Check default web server
* if IIS (Internet Information Services), the default folder is `C:\inetpub`
