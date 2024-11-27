Security Dashboard Obvervatrion

![[Pasted image 20241127175332.png]]
## Web01

uses wget to pull powerview.ps1, Rubeis.exe, PsExec54.exe
created at 05:49:19.687
![[Pasted image 20241127184402.png]]

used psexec to send a file to apsvr01
created at 05:49:19.476
![[Pasted image 20241127184711.png]]

user powerview to perform recon 
created at 05:48:22.096
![[Pasted image 20241127184933.png]]

kerberoast with rubeus 
created at 05:48:32.016
![[Pasted image 20241127190347.png]]



psexec used to execute the aappmet6.exe on the appsrv06 remote host
created at 05:49:35.830
![[Pasted image 20241127185637.png]]

used psexec to move lateraly with found credentials
created at 05:49:35.694
![[Pasted image 20241127185948.png]]

## appsrv06
lateraly moved from the web server 01 to her with the user appmgadm 
created on 05:49:19.945

![[Pasted image 20241127181621.png]]

wget to pull down aappmet6.exe
created at 05:49:20.175
![[Pasted image 20241127175954.png]]


used psexec to run the aappmet6.exe
created at 05:49:35.330
![[Pasted image 20241127180346.png]]

started notpad service with aappmet6
created at 05:49:40.000
![[Pasted image 20241127180513.png]]

accesses lsass with aappmet6 because it is already admin
created at 05:49:38.355
![[Pasted image 20241127180611.png]]

create remote thread in notpad.exe
created at 05:49:40.000
![[Pasted image 20241127180735.png]]




