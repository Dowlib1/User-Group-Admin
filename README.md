# User-Group-Admin
This project will help you understand Advanced linux commands featuring; how to Create and manage users, Group(s) and how to  modify group, user privileges and read write and execution access to files and direcotires...

### 1. Linux Numeric representation of permission

Open your terminal and run:
```bash
ls -latr
```
no permission=0 read=4 write=2 execute=1
rw= 4+2 =6
wx=2+1 =3
rwx=4+2+1 =7
![display of linux num represention](images/edit.png)

##shorthand representation of permision
To explore this take this example; create a file

![create a file](images/touch.png)
### 2. Create a File

To create a file:
```bash
touch script.sh
```

![Created note.sh](images/script.png)
![create not,txt](images/teouch.png)

### 3. check permision level to file

![view access level](images/latr.png)
Press

`
ls -latr script.sh
 `
 Now change or grant execution access for all users.
 using
` chmod +x script.sh`

![edit acccess level](imagess/777.png)


![heirarchica level management](imagess/755.png)
### 4. Now check what the permission looks like.
`ls -latr script.sh`

![view current access level](images/755.png)

another example;
 ```
chmod 755 script.sh
 ```

 ### 5 do thesame for noted .txt
 another example;
 ```
 chmod 777 note.sh
 ```
![view current access level](images/777.png)
 `ls -latr notes.sh`
 
![file detail](images/777.png)

### 6. Change the ownership of a file wtih respect to  user, group

![file permission](images/adduse.png)

run:
```bash
chown john:developer filename.txt
```

![create user](images/adduse.png)


### 8. Superuser privileges

To switch users;
```bash
sudo -i

```
![get info](images/-i.png)
Input `exit` to leave the shell
![Screenshot](images/ediit.png)


### 9 . Create user

```
sudo adduser johndoe
```


![make a new user](images/useradgrp.png)

### 10. Grant administrative priviledges for user johndoe
![highlghted in green](images/johnd.png)
```
sudo usermod -aG sudo johndoe

```


### 11. change password for user johndoe
![Highlightede in yellow](images/johnd.png)
```
sudo passwd johndoe

```

Log out to login to johndoe:
use `su johndoe`
![highlighted in red](images/johnd.png)

### 12. Creating group and adding users to group
```
sudo groupadd developers


```
![add user to group](images/addgroup.png)

```
sudo usermod -aG developers johndoe

```

![Screenshot](images/adduse.png)

## Verify group users;
```
id johnoe

```
##Delete user
```
sudo userdel bamilola
```
### 13 Group permission
![mange permission](images/idjohn.png)
```
sudo chown :developers /home/tandemvuu/Document
```
![give permit](images/777.png)
```


```sudo chmod g+rw /home/tandemvuu/Document

```
 ![give access ](images/groupaccess.png)
## Miscellaneous tasks
create other users
![Screenshot](images/addgroup.png) 

create devop group
![create a new group](images/addgroup.png)

create folders for each users
![new flder](images/mkdirforuser.png)

## add userss to group
![new grp&users](images/addusergroup.png)
![Screenshot](images/filepermit.png)

 give access to devop group
 ![add picture](images/gdpir.png)

 ![access as asset](images/groupaccess.png)
 ![Screenshot](images/mkdirforuser.png)
Refer to the included screenshots for visual guidance on these steps.

---

## License

This repository is open source and free to use for educational purposes.
