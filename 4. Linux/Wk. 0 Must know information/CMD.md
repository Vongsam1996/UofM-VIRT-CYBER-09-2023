Commands for navigating a file directory:
- `pwd`: Displays the current working directory.
- `ls`: Lists the directories and files in the current directory.
- `cd`: Navigates into a directory.
- `cd ../`: Navigates out of a directory.
- `clear`: Clears out the terminal history on the page.

Commands for making and removing files and directories:
- `mkdir`: Creates a new directory.
- `rmdir`: Removes a directory.
- `touch`: Creates an empty file.
- `rm`: Removes a file.

Commands for moving and copying files:
- `cp`: Copies files.
- `mv`: Moves files.

Commands for previewing files
- `more`: Shows a file one page at a time. Space bar is used to move from page to page.
- `less`: Similar to `more`, but allows scrolling up and down pages.
- `head`: Previews the top 10 lines of a file.
- `tail`: Previews the bottom 10 lines of a file.

Commands for concatenating and redirecting:
- `cat`: Concatenates and combines multiple files together.
- `>`: Writes to a file, and overwrites file if the file name already exists.
- `>>`: Writes to a file, and appends to the file if the file name already exists.

**Replacing values (text, files, etc)**
-sed s/(old value)/(replacement value)/

**Printing/ only showing certain data**
-awk -F(delimiter) '{print $(field_number)}'

**Changing ownerships**
chown user:group [file name]

**Having access to sysadmin changes**
sudo cmd [file name] 

**Installing packaging** 
sudo apt [file name]

**How to add a user to a group**
sudo usermod -G [Group name]  [username]

**Seeing ID groups**
id 

**Adding a group**
sudo addgroup [group name]

**add user** 
sudo useradd [name] 

**Add user to groupgroup**
sudo groupadd [group name]
sudo usermod -G [group name]  [user]
- will delete user from other groups and add to new group
- Will not delete their own group 

**Changing permission of files**
- sudo chown username:username file name

sudo usermod -aG [group name]  [username]
- will add username in group and keep other groups

to change the owner of a folder 
sudo chown new_owner_username:group_name folder_path

**give group to permission**
chown user:group [folder] 

NOTE: sudo chown :[group name]  [folder]
- This will add everyone in the group name 


# if [ <condition> ]
# then
#   <run_this_command>
#   <run_this_command>
#   <run_this_command>
# fi

[4:39](https://uofmvirtcyber-vmg7105.slack.com/archives/C05KRLVH0QN/p1697758773750389)

#!/bin/bash

#Use this template to avoid syntax headaches

 if [ <condition> ]
 then
   <run_this_command>
   <run_this_command>
   <run_this_command>
 fi

#!/bin/bash
# Basic if statement
# if [ <condition> ]
# then
#   <run_this_command>
#   <run_this_command>
#   <run_this_command>
# fi
# if [ <condition> ]
# then
#   <run_this_command>
# else
#   <run_this_command>
# fi
# if [ <condition1> ] && [ <condition2> ]
# then
#   <run_this_command>
# else  
#   <run_this_command>
# fi
# if [ <condition1> ] || [ <condition2> ]
# then
#   <run_this_command>
#   <run_this_command>
#   <run_this_command>
# fi
# number variables
x=5
y=100
# string variables
str1='this is a string'
str2='this is different string'
# If $x is equal to $y, run the echo command.
if [ $x = $y ]
then 
  echo "X is equal to Y!"
fi
# If x is not equal to y, exit the script
if [ $x != $y ]
then 
  echo "X does not equal Y"
fi
# If str1 is not equal to str2, run the echo command and exit the script.
if [ $str1 != $str2 ]
then 
  echo "These strings do not match."
  echo "Exiting this script."
  exit
fi
# If x is greater than y, run the echo command - only works for integer values
if [ $x -gt $y ]
then
  echo "$x is greater than $y".
fi
# check if x is less than y - only works for integer values
if [ $x -lt $y ]
then 
  echo "$x is less than $y!"
else
  echo "$x is not less than $y!"
fi
# check if $str1 is equal to 'this string' AND $x is greater than $y
# only works if x and y are integers
if [ $str1 = 'this string' ] && [ $x -gt $y ]
then
  echo "Those strings match and $x is greater than $y!"
else
  echo "Either those strings don't match, or $x is not greater than $y"
fi
# check if $str1 is equal to str2 OR $x is less than $y
# only works if x and y are integers
if [ $str1 != $str2 ] || [ $x -lt $y ]
then
  echo "Either those strings don't match OR $x is less than $y!"
else
  echo "Those strings match, AND $x is not less than $y"
fi
# check for the /etc directory
if [ -d /etc ]
then
  echo "The /etc directory exists!"
fi
# check for my_cool_folder
if [ ! -d /my_cool_folder ]
then 
  echo "my_cool_folder isn\'t there!"
fi
# check for my_file.txt
if [ -f /my_file.txt ]
then
  echo "my_file.txt is there"
fi
# if sysadmin is running this script, then run an echo command
if [ $USER != 'sysadmin' ]
then 
  echo "You are not the sysadmin!"
  exit
fi
# if the uid of the user running this script does not equal 1000, run the echo command
if [ $UID -ne 1000 ]
then
  echo "Your UID is wrong"
  exit
fi
# if sysadmin is running this script, run the echo command
if [ $(whoami) = 'sysadmin' ]
then
  echo "You are sysadmin!"
fi