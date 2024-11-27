
file created:

![[Client04_phase1_fileCreate.png]]

process create:

![[Client04_phase1_procCreatre.png]]

create tmp file

![[Client04_phase1_fileCreate2_tmpFile.png]]

process created for tmp file
![[Client04_phase1_procCreate2_tmpFile.png]]

remote thread created for notepad
![[Client04_phase1_remoteThreadCreate.png]]

tmp process terminated for tmp

![[Client04_phase1_procTerminate_tmpFile.png]]

process create from notpad to cmd.exe
![[Client04_phase1_procCreate3_cmd.exe.png]]


cmd.exe then create as process to use powershell command to wget a file from remote server

![[Client04_phase1_procCreate4_psExe.png]]

cmd to add a registry run key to execute the HPP.exe every time the user logs in
![[Client04_phase1_procCreate5_regEdit.png]]

the attacker then used wget to get another executable. the source IP for this was 192.168.55.38 indicating it was an request internal to the network however the host is not being tracked by the logs

output file for request one is `HPP.exe`

![[Pasted image 20241127101054.png]]


=====================

![[Pasted image 20241127094434.png]]


Privilege escalation --

