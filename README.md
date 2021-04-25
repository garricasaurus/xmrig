# xmrig portable configuration

## how to use

### download & install xmrig

For example for Ubuntu Server:

```
wget https://github.com/xmrig/xmrig/releases/download/v6.12.1/xmrig-6.12.1-bionic-x64.tar.gz
tar --strip-components=1 -zxf xmrig-6.12.1-bionic-x64.tar.gz
sudo mv xmrig /usr/bin/xmrig
```

### clone the repository

```
sudo git clone https://github.com/garricasaurus/xmrig
```

### setup config & log location

```
sudo mkdir -p /var/lib/xmrig
sudo mkfir -p /var/log/xmrig
sudo cp xmrig/config.json /var/lib/xmrig
```

### enable & start the systemd service

```
sudo cp xmrig/xmrig.service /etc/systemd/system/xmrig.service
sudo systemctl daemon-reload
sudo systemctl enable xmrig
sudo systemctl start xmrig
```

