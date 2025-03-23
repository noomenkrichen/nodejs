## Check current OS version:
```bash
lsb_release –a
```
or
```bash
cat/etc/os-release
````
or
```bash
cat /proc/version
```
or
```bash
hostnamectl
```
or
```bash
uname –a
```

## Ubuntu Servers
### 1.	Install ubuntu-release-upgrader-core if it is not already installed:
```bash
sudo apt-get install ubuntu-release-upgrader-core
```
2.	Edit /etc/update-manager/release-upgrades and set Prompt=normal (originally it is Prompt=lts)
```bash
sudo nano /etc/update-manager/release-upgrades
```
3.	Launch the upgrade tool:
```bash
do-release-upgrade
```
4.	Follow the on-screen instructions.
