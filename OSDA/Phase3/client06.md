Security Dashboard Observations
![[Pasted image 20241127175208.png]]


anonyumous login from client04
created at 01:14:27.934 
![[Pasted image 20241127143508.png]]


they then logged on with clisvc account which has admin level priv
created at 01:14:29.956
![[Pasted image 20241127143751.png]]

a powershell script performs a wget to pull another file
created at 01:14:33.080 by clisvc
Query `wget` filter `host.name: client06`
![[Pasted image 20241127145133.png]]

met_c6.exe then created a process for powershell that executed an obviscated sting that requires reordering
created at 01:15:14.006 
Query `met_c6.exe` filter `host.name: client06`
![[Pasted image 20241127150138.png]]

met_6c.exe then created the notpad process
created at 01:15:18.087
Query `met_c6.exe` filter `host.name: client06`
![[Pasted image 20241127150254.png]]

met_c6.exe targets lsass.exe and targeting the system user
created  01:15:18.087
Query `met_c6.exe` filter `host.name: client06`
![[Pasted image 20241127150549.png]]

met_c6.exe created remote thread to notpad.exe
created at 01:15:18.087
Query `met_c6.exe` filter `host.name: client06`
![[Pasted image 20241127150748.png]]

notepad create a process for cmd.exe
created at 01:15:23.190
Query `notepad.exe` filter `host.name: client06`
![[Pasted image 20241127151027.png]]

cmd.exe then creates a powershell process
created at 01:15:23.190
Query `cmd.exe` filter `host.name: client06`
![[Pasted image 20241127151304.png]]

created a two powershell files
01:15:23.190 `C:\Users\clisvc\AppData\Local\Temp\__PSScriptPolicyTest_xgijkux4.3ak.ps1`
01:15:24.213 `C:\Users\clisvc\AppData\Local\Temp\__PSScriptPolicyTest_vidpvrgi.qqx.ps1`