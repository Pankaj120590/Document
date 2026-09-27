#docs
User Management

[root@server0Desktop]#

useradd sky
passwd sky

NOTE: Whenever any user is created bydefault three folder gets created.

Here is the folders

vim /etc/passwd
vim /etc/group
vim /etc/shadow

Inside passwd directory user information is saved
# Group information of user is saved inside group directory
#Password information of user is saved inside shadow directory

To add secondary group
# groupadd sysadmin
