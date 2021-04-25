# Extra steps for Azure extra small VM

Add a 2G swapfile:

```
sudo dd if=/dev/zero of=/swapfile bs=1M count=2048 status=progress
sudo chmod 600 /swapfile
sudo mkswap /swapfile
sudo swapon /swapfile
```

Persist swapfile in `/etc/fstab`:

```
/swapfile   none   swap   defaults 0 0
```

Adjust swappiness in `/etc/sysctl.d/99-swappiness.conf`

```
vm.swappiness=10
```
