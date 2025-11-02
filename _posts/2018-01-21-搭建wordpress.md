---
title: 快速搭建wordpress
layout: post
tags:
  - wordpress
category: it
---
# install lnmp
```bash
screen -S lnmp
wget http://soft.vpser.net/lnmp/lnmp1.6.tar.gz -cO lnmp1.6.tar.gz && tar zxf lnmp1.6.tar.gz && cd lnmp1.6 && ./install.sh lnmp
ln -s /usr/local/nginx/conf/vhost/
Or
screen -S oneinstack
wget http://mirrors.linuxeye.com/oneinstack-full.tar.gz && tar xzf oneinstack-full.tar.gz && cd oneinstack && ./install.sh

```
# download wordpress
```bash
cd /home/wwwroot/
wget http://wordpress.org/latest.tar.gz
tar -xzvf latest.tar.gz
chown -R www:www wordpress
```
# mysql
```bash
mysql -u root -p
CREATE DATABASE wordpress; 
GRANT ALL PRIVILEGES ON wordpress.* TO "username"@"localhost"
    
    -> IDENTIFIED BY "password";
FLUSH PRIVILEGES;
exit
```
