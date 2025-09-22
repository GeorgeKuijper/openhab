# OPENHAB - a vendor and technology agnostic open source automation software for your home.

[openhab/openhab](https://hub.docker.com/r/openhab/openhab/)
# According to website
```shell
sudo groupadd -g 9001 openhab
sudo useradd  -g 9001 openhab
sudo usermod -a -G openhab pi

#sudo mkdir -p /opt/openhab/{openhab_addons,openhab_conf,openhab_userdata}
?? sudo mkdir -p /opt/openhab/{addons,conf,userdata}
??sudo chown -R openhab:openhab /opt/openhab
?? sudo chmod -R 775 /opt/openhab
```

# Maybe not needed
```shell
sudo groupadd -g 9001 openhab
sudo useradd -r -s -u 9001 /sbin/nologin openhab
sudo usermod -a -G openhab openhab

sudo mkdir -p /opt/openhab/{addons,conf,userdata}
sudo chown -R openhab:openhab /opt/openhab
#sudo chmod -R 775 /opt/openhab
```

```shell
# List all groups
getent group
# List all users
getent passwd
```

# 20250922
```shell
# Create group openhab with gid 9001
sudo groupadd -g 9001 openhab
# Create user openhab with uid 9001 without interactive logon possibilities (leads to useradd warning: openhab's uid 9001 is grater than SYS_UID_MAX 999 )
sudo useradd -u 9001 -g openhab -r -s /sbin/nologin openhab
# Add user open hab (9001) to group openhab (9001)
sudo usermod -a -G openhab openhab
# Add user openhab (9001) to group docker (992)
sudo usermod -a -G docker openhab

sudo mkdir -p /opt/openhab/{conf,userdata,addons}
sudo chown -R openhab:openhab /opt/openhab
```
