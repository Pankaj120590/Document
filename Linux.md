# Title: User Management

[root@server0Desktop]#

The useradd command is a low-level, command-line utility used in Linux and Unix-like operating systems to create and initialize new user accounts.

sudo useradd username

*useradd user1*  
*passwd user1*
---

NOTE: When you run useradd, the system modifies critical configuration files like **/etc/passwd** (user details), **/etc/shadow** (encrypted passwords), and **/etc/group** (group definitions) to register the new identity.


- User account information is stored in the `/etc/passwd` file.
- Group information for users is stored in the `/etc/group` file.
- Password information for users is stored in the `/etc/shadow` file.

# To create/add secondary group
**groupadd sysadmin**


# To add user in "Group or Secondary group"

**usermod -G sysadmin sky**  
**usermod -G sysadmin student** 

- -G :           Indicates secondary group  
- sysadmin:      Group name  
- sky & student: Username

# To create group
**groupadd aws**

# To add a user in secondary group
**usermod -G aws sky**

# To add a single user in multiple group
**usermod -aG sysadmin sky**
- -a: appened means to include/appened the user in the secondary group  

- vim /etc/group

# To delete a user/group member from the secondary group.
**groupmems -g sysadmin -d sky**

# To delete a group
**groupdel aws**  
**vim /etc/group**


# To delete user
**userdel sky**


# To remove a folder of a user from the directory.
**rm -rf /home/sky**  
**ls -ll /home**

Whenever a user is created bydefault the user directory is created inside /home directory over username. 
To delete a user and their home directory in Linux, run the command sudo userdel -r username in your terminal

# sudo userdel -r username

1. `:Replace username with the actual name of the user you want to delete.
2. The -r option tells the system to remove the user's home directory and mail spool

# userdel -r sagar


#usermod -c php sky
-c: comment 

actual user is sky but when the user will login it will see php user

To lock user 
# usermod -L sky

To unlock user
# usermod -U sky

To rename username
# usermod -l kpl ipl

kpl: new name
ipl: old name


# useradd sky
# rm -rf /home/sky


# usermod -c newname oldname
# usermod -c php sky
-c: comment
sky: old name
php : new name





