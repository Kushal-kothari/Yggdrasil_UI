# Yggdrasil_UI

### Steps to install:

```T
sudo apt-get install dirmngr
```
```T
gpg --fetch-keys https://neilalexander.s3.dualstack.eu-west-2.amazonaws.com/deb/key.txt
```
```T
gpg --export 569130E8CA20FBC4CB3FDE555898470A764B32C9 | sudo apt-key add -
```
```T
echo 'deb http://neilalexander.s3.dualstack.eu-west-2.amazonaws.com/deb/ debian yggdrasil' | sudo tee /etc/apt/sources.list.d/yggdrasil.list
```
```T
sudo apt-get update
```
Install Yggdrasil:
```
sudo apt-get install yggdrasil
```
Configuration will be generated automatically into /etc/yggdrasil.conf when the package is installed, and the Yggdrasil service will automatically be installed into systemd.

Enable and start the service after install/upgrade:
```T
sudo systemctl enable yggdrasil
sudo systemctl start yggdrasil
```
Now in order to run this script you need to be the root user.Simply do :
```
sudo python3 surge.py
```
