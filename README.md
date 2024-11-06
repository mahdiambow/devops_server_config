### 1: Update the Apt

`sudo apt update 
`

`sudo apt dist-upgrade`

`
sudo apt autoclean`

### 2: Add User

`adduser <USERNAME>
`

`usermod -aG sudo <USERNAME>`

### 2: Connect To The Created User

`ssh username@SERVER-IP
`

### 3: Create SSH KEY

`ssh-keygen
`

`ssh-copy-id -i ~/.ssh/name_id_rsa.pub username@SERVER-IP
`

### 4: SSH With Name (No IP)

1: `sudo vi ~/.ssh/config
`

2: paste this :

```plaintext
Host myserver
    HostName myserver.local
    User username
    IdentityFile ~/.ssh/id_rsa
    Port 22
```

### 5: Turn Off The Root Login

`sudo vi /etc/ssh/sshd_congfig
`

##### Put "No" Next To The PermitRootLogin

`PermitRootLogin no
`
