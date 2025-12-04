# simpel-ssh-server

(for arch linux)

## installing openssh

```bash
sudo pacman -S openssh
```

## starting ssh 

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
