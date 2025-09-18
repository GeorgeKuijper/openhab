# OPENHAB - a vendor and technology agnostic open source automation software for your home.

[openhab/openhab](https://hub.docker.com/r/openhab/openhab/)

```shell
sudo groupadd -g 9001 openhab
sudo useradd  -g 9001 openhab
sudo usermod -a -G openhab pi

sudo mkdir -p /opt/openhab/{openhab_addons,openhab_conf,openhab_userdata}
sudo chmod -R 775 /opt/openhab
```