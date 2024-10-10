24.10.08  20.47
tags: [[linux]] [[web]] 

# OS command line, commands

works for linux and some are for windows powershell

- `ls - lists directory  
- `ls -a
- `ls -l 
- `pwd  `  print working directory 
- `cd`       change directory
- `cd .. `  go to prev folder 
- `cd ~`   go to the starting home directory 
- `mkdir ` create new folder 
- `history`  lists cmds used before
- `mv - rename 
- `Rm or remove`  delete, doesn't move to the recycle bin 

- `Get-help`  displays help for powershell  
- `cat` view contents of a file 
- `more`  - views content one page at a time (Enter - advances a line, space - advances a page 
- `Q` - quit the more and back to  shell 
- `Get-Content filename -head 5`       - view partial 
-                                         `-tail  5 

## in Linux 
- `less ` - does similar things to more but have more functionality 
	- Up and down keys 
	- G moves to the end of a text file 
	- /word-search 
	- Q -quit out of less 

- `head - first 10 lines of a file 
- `tail - last  

## Windows - powershell 

- `Get-alias -  
- `Get-ChildItem` - similar fun to ls and dir 
- `Select-string -filter` for windows,  `grep` for linux 
- `Echo woof > dog.txt` - creates a text file and writes woof to it 
	 - `>`    a redirector 
	 - `>>`   append 

- `|` Send the output of one cmd to input of another cmd
- Takes the output of words.txt and prints out words which have st in them then writes the output on a new created file called st_words.txt. 
	- `Cat words.txt | select-string st > st_words.txt 

1: Stdout - the output 
2: Stderr - the error 

`rm securefile 2 > error.txt 
- `Writes the error message to the text file 

$null 

Linux - similar to windows 
/dev/null 

## Users and Administrators 
Linux 
- `Sudo su` -  Makes us a root user 
- You can view who has access to run sudo by viewing the /etc/group.  
- This is also how you view memberships for all groups.   
From <[https://www.coursera.org/learn/os-power-user/lecture/ke9fl/linux-users-superuser-and-beyond](https://www.coursera.org/learn/os-power-user/lecture/ke9fl/linux-users-superuser-and-beyond)>    



- `Net user username password`   Change local password in powershell W 
- `Net user username *`  Then on a new line the password 
- A better way for the above W `Net user username logonpasswordchg:yes 
- The problem with the above approach is I would know a users password, so this cmd will require the user to change their password on the next login W 
- `Cat /etc/passwd` To view users on our machine l 
- `Passwd username` Changing password in l 
- `Sudo Passwd -e username` To expire a users password and force them to change in on next logon in l 

adding new users using cli in W
- `Net user newusername password /add  
- `Net user newusername * newlinepassword 

- `Net user username /logonpasswordchg:yes` Forcing users change their password on the next logon W 
- `Net user newusername password /add /logonpasswordchg:yes` And combining the above 2 cmds W 

- `Remove-localuser username 
- `Net user username /del` Removing user W 

- `Get-localuser` Shows users on the machine w 
- `Sudo useradd username` Add user L 
- `Sudo userdel username`  Delete user L

## Permissions  

- Files and directory permissions are assigned using ACL - Access control lists  
    
- Eg DACLS(Discretionary), SACLS(system - it makes event log file to note everytime a user accesses a file or folder) 
    
- You can have write permission with out having a read permission 
    
- Iist folders permission is an alias for read and write permission, If you tick one the other will be automatically ticked also 
    
- Modify is an umbrella 
- 
- `Icacls - 
    
- `Icacls /? 
    - help  
        

## Software distributions 

Linux software packages 
- Debian package - ubuntu 

To install a package     
`Sudo dpkg - I filename   

To remove     
`Sudo dpkg -r filename   

To list install pkgs   
`Dpkg -l    
`Dpkg     

Archive using powershell   
`Compress-archive -path paththefilesin paththearchivewillbe   

Archive in linux   
First install 7z   

To extract   
`7z e filenametoextract   

Parted command?   

View disk usage of certain directory in linux   
`Du -h   

To view free space in ur entire system in linux, the h flag specifies to present in human readable form   
`Df -h   

If you want to check the status of the self-healing process on your computer, you can open up an administrative command prompt and use the fsutil tool like this.   
From <[https://www.coursera.org/learn/os-power-user/lecture/aXBeM/windows-filesystem-repair](https://www.coursera.org/learn/os-power-user/lecture/aXBeM/windows-filesystem-repair)>    

In Linux, you can view block devices and file systems attached to your system using the lsblk command.   
From <[https://googlecoursera.qwiklabs.com/focuses/31883177?parent=lti_session](https://googlecoursera.qwiklabs.com/focuses/31883177?parent=lti_session)>    

## Processes 
Terminate a process in powershell   
`taskkill /pid pidnumber   

terminate multiple processes   
`taskkill /pid 1230 /pid 1241 /pid 1253   

more on taskkill   
[https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/taskkill](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/taskkill)   

show processes running on linux   
`ps -x   

show full processees   
`ps -ef   

lists process with the name chrome     
`ps -ef | grep chrome   

kill a process in linux   
`sudo kill pidno   

list processes in powershell   
`get-process  


# Reference

