Security Dashboard Overview of this phase
![[Pasted image 20241127175051.png]]


another ps script block pulled down w1.exe and met.exe from remote server

cmd injection through a field in the webpage executing a wget for met.exe
created at 04:11:55.135
query `met.exe` filter `host.name: web01`
![[Pasted image 20241127163348.png]]

cmd injection through a field in the webpage executing met.exe binary
created at 04:12:20.333
query `met.exe` filter `host.name: web01`
![[Pasted image 20241127172835.png]]

met.exe create notpad.exe process
created at 04:12:21.354
query `met.exe` filter `host.name: web01`
![[Pasted image 20241127173132.png]]

met create remote thread to notepad.exe
created at 04:12:21.354
query `met.exe` filter `host.name: web01`
![[Pasted image 20241127163150.png]]


met.exe accessed lsass as the user is already SYSTEM so it can
created at 04:12:21.354
query `met.exe` filter `host.name: web01`
![[Pasted image 20241127164034.png]]


the actor attaind the creds for `FISHCO\webadmin`


created at 04:12:26.104
query `W1` filter `host.name: web01`

![[Pasted image 20241127162558.png]]

w1.exe persistence, the C:\scripts\service_check.ps1 script runs very frequently and can execute the w1.exe as a means of persistence every 5 seconds approximately 
created at 04:12:26.397
![[Pasted image 20241127173941.png]]

w1.exe then creates a remote threat to notpad.exe
created at 04:15:47.224
query `W1.exe` filter `host.name: web01`
![[Pasted image 20241127162729.png]]

then uses w1.exe to access lsass also this time as the `webadmin` user
created at 04:15:47.224
query `W1.exe` filter `host.name: web01`
![[Pasted image 20241127174313.png]]









