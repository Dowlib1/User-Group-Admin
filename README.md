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
![display of linux num represention](image/edit.png)

##shorthand representation of permision
To explore this take this example; create a file

![create a file](image/touch.png)
### 2. Create a File

To create a file:
```bash
touch script.sh
```

![Created note.sh](image/script.png)
![create not,txt](image/teouch.png)

### 3. check permision level to file

![view access level](image/latr.png)
Press

`
ls -latr script.sh
 `
 Now change or grant execution access for all users.
 using
` chmod +x script.sh`

![edit acccess level](images/777.png)


![heirarchica level management](images/755.png)
### 4. Now check what the permission looks like.
`ls -latr script.sh`

![view current access level](image/755.png)

another example;
 ```
chmod 755 script.sh
 ```

 ### 5 do thesame for noted .txt
 another example;
 ```
 chmod 777 note.sh
 ```
![view current access level](image/777.png)
 `ls -latr notes.sh`
 
![file detail](image/777.png)

### 6. Change the ownership of a file wtih respect to  user, group

![file permission](image/adduse.png)

run:
```bash
chown john:developer filename.txt
```

![create user](image/adduse.png)


### 8. Superuser privileges

To switch users;
```bash
sudo -i

```
![get info](image/-i.png)
Input `exit` to leave the shell
![Screenshot](image/ediit.png)


### 9 . Create user

```
sudo adduser johndoe
```


![make a new user](image/useradgrp.png)

### 10. Grant administrative priviledges for user johndoe
![highlghted in green](image/johnd.png)
```
sudo usermod -aG sudo johndoe

```


### 11. change password for user johndoe
![Highlightede in yellow](image/johnd.png)
```
sudo passwd johndoe

```

Log out to login to johndoe:
use `su johndoe`
![highlighted in red](image/johnd.png)

### 12. Creating group and adding users to group
```
sudo groupadd developers


```
![add user to group](image/addgroup.png)

```
sudo usermod -aG developers johndoe

```

![Screenshot](image/adduse.png)

## Verify group users;
```
id johnoe

```
##Delete user
```
sudo userdel bamilola
```
### 13 Group permission
![mange permission](image/idjohn.png)
```
sudo chown :developers /home/tandemvuu/Document
```
![give permit](image/777.png)
```


```sudo chmod g+rw /home/tandemvuu/Document

```
 ![give access ](image/groupaccess.png)
## Miscellaneous tasks
create other users
![Screenshot](image/addgroup.png) 

create devop group
![create a new group](image/addgroup.png)

create folders for each users
![new flder](image/mkdirforuser.png)

## add userss to group
![new grp&users](image/addusergroup.png)
![Screenshot](image/filepermit.png)

 give access to devop group
 ![add picture](image/gdpir.png)

 ![access as asset](image/groupaccess.png)
 ![Screenshot](image/mkdirforuser.png)
Refer to the included screenshots for visual guidance on these steps.

---

## License

This repository is open source and free to use for educational purposes.
