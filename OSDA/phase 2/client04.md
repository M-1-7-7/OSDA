still as user `j.moore`


adversary did a wget to pull 3 new files, once they where down her restarted the machine with a `shutdown` event
query `shutdown`
created at 00:02:14.371 as j.moore
![[Pasted image 20241127125258.png]]

then with the persistence mechanism being the run key found in phase1, i assume it triggers the execution of these binaries at system level privilege.

the system was restarted again as System user and may explain why `met_hp.exe process terminated` occurred initially 

![[Pasted image 20241127125819.png]]

=================================================


runs wget for `launch_hp.exe` file and outputs it to the file name of `HP.exe
created  at 00:02:11.703 as j.moore
query `wget`
![[Client04_phase2_procCreate1_wget_launch_hpexe.png]]
create at 00:03:23.907 as SYSTEM
![[Pasted image 20241127120520.png]]



=================================================
runs wget for `met_hp.exe` file and outputs it to the file name of `met_hp.exe
created at 00:02:12.873 as j.moore

query `wget`
![[Client04_phase2_procCreate2_wget_met_hpexe.png]]

HP.exe executed the met_hp.exe as SYSTEM
created at 00:03:23.962 as SYSTEM
query `met_hp.exe`
![[Pasted image 20241127120815.png]]

cmd.exe executes met_hp.exe as SYSTEM
created at 00:03:26.097 as SYSTEM
query `met_hp.exe`
![[Pasted image 20241127122456.png]]

met_hp.exe then created a cmd process
created at 00:04:00.317 as SYSTEM
query `met_hp.exe`
![[Pasted image 20241127121603.png]]

met_hp.exe process terminated
created 00:04:08.275 as SYSTEM
query `met_hp.exe`
![[Pasted image 20241127122821.png]]

HP.exe executed met_hp.exe 
created at 00:05:25.738 as SYSTEM
query `met_hp.exe`
![[Pasted image 20241127121849.png]]

cmd.exe executes met_hp.exe as SYSTEM
created at 00:05:26.097 as SYSTEM
query `met_hp.exe`
![[Pasted image 20241127122646.png]]

met_hp.exe process terminated
created at 00:05:52.082 as SYSTEM
query `met_hp.exe`
![[Pasted image 20241127122929.png]]


=================================================
runs wget for `met_hpp.exe` file and outputs it to the file name of `met_hpp.exe
created at 00:02:13.806 as j.more
query `met_hpp.exe`
![[Client04_phase2_procCreate3_wget_met_hppexe.png]] `

made network connection to .192.168.55.38 as SYSTEM on port 8889
created at 00:05:30.212 as SYSTEM
query `met_hpp.exe`
![[Pasted image 20241127123252.png]]

from client04 (this box) the attacker attempt to pivots to DC over smb
created at 00:06:08.554 through to 00:06:13.601 as SYSTEM
query `met_hpp.exe`
![[Pasted image 20241127123510.png]]

quite a bit of traffic to mail1 as well
