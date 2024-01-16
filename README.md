# xrdp-ubuntu

 Update the list of available packages using the following command
 
```
sudo apt update
```

### Install the xfce and xfce-goodies packages

```
sudo apt install xfce4 xfce4-goodies -y
```

### Install xrdp 
```
sudo apt install xrdp -y
```
### Start xrdp service

```
sudo systemctl status xrdp
```
### Set Up a Firewall with UFW

Ensure IPV6 is set to yes in below file
```
sudo nano /etc/default/ufw
```

### It should look like this:
```
IPV6=yes
```
### Setting Up Default Policies
```
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

### Allowing SSH Connections

```
sudo ufw allow ssh
sudo ufw allow 3389
```

### Enabling UFW
```
sudo ufw enable
```

### Specific Port Ranges
```
sudo ufw allow 6000:6007/tcp
sudo ufw allow 6000:6007/udp
```
