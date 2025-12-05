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

To check the owner of an file 

```bash
stat -c %U /media/sf_Shared/
```

to check Access right from a user

```bash
stat -c %A /media/sf_Shared/
```

