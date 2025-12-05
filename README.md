# simpel-ssh-server

(for arch linux)

## installing openssh

```bash
sudo pacman -S openssh
```

## starting ssh 
Password and account management tool suite with support for shadow files and PAM
```bash
sudo systemctl start sshd
```

## autosart ssh on boot

```bash
sudo systemctl enable sshd
```

## Setting up firewall to open up a port

```bash
sudo ufw allow {port}/tcp
```

## Connecting with/to ssh
 
 To show the ip addres to connect with:

```
ip addr show
```

The line that starts with inet contains the ip addres


To connect to the ssh server excecute:

```bash
ssh username@ip-address
```

# Configurering Users 

## Checking User/groups 

To check the owner of an file 

```bash
stat -c %U /media/sf_Shared/
```

to check Access right from a user

```bash
stat -c %A /media/sf_Shared/
```

to check the owned files by a user 

```bash
find / -user user
```

to Check the owned files by a group

```bash
find / -group groupname
```

## User management 

to add a new user, use the useradd command:

```bash
useradd -m -G *additional_groups* -s login_shell username
```

-m / --create-home creates a home for the user : /home/username

-G / --groups to add to given groups

-s / --shell a path to the user's 

**useradd will create a group called like the username and make it the Default group for the Created user**

to set the password to the newly creaded user 

```bash
passwd username
```

## To Config Groups

By Default a group from a user can only read/write the files they created themself.
To change the abbilty to read/write other directorys use

```bash
chmod g+s directory
```

## Program for Password and account management tool suite.

Install

```bash
pacman -S shadow
```

# Quelle 

https://wiki.archlinux.org/title/Users_and_groups
