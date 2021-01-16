## Prerequsities
```bash
sudo apt-get update
sudo apt-get upgrade
```

### Install Apache
```bash
sudo apt-get install apache2
```

### Install MySQL
``` bash
sudo apt-get install mysql-server
```
###### Secure your MySQL server
``` bash
sudo mysql_secure_installation
```

### Install PhpMyAdmin
``` bash
sudo apt install phpmyadmin php-mbstring php-gettext
```
###### enable mbstring php extension and restart Apache service 
```bash
sudo phpenmod mbstring
sudo systemctl restart apache2
```

### Install PHP
```bash
sudo apt-get install php libapache2-mod-php
```
###### Install Redis PHP Extension
```bash
sudo apt-get install php-redis
```
###### Install xdebug PHP Extension
```bash
sudo apt-get install php-xdebug
```
### Install Java using the Ubuntu Open JDK binaries
###### To install Ubuntu Java Open JDK version 11 execute:
``` bash
sudo apt install openjdk-11-jdk
```
###### and for Java Open JDK 8 run:
```bash
sudo apt install openjdk-8-jdk
```
### Installing Redis
```bash
sudo apt-get install redis-server
```
###### to enable Redis to start on system boot
```bash
sudo systemctl enable redis-server.service
```

### Install CopyQ Clipboard Manager
```bash
sudo add-apt-repository ppa:hluk/copyq
```

### Install Composer
```bash
sudo apt-get install composer
```

### Install pip (pip is a Python package management tool)
```bash
sudo apt-get install python-pip
```
##### Install pip3
```bash
sudo apt-get install python3-pip
```
##### Update pip3
```
sudo pip3 install --upgrade pip
```

### Install python-mysqldb
```bash
sudo apt-get install python-mysqldb
```
### Install mysqlclient
```bash
sudo pip3 install mysqlclient

```

### Install Nodejs 14.x
```
curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -

sudo apt-get install nodejs

nodejs --version
npm --version
```

### Insall PHP and Nginx
```
sudo apt install software-properties-common

sudo add-apt-repository ppa:ondrej/php
sudo apt install php7.3 php7.3-common php7.3-opcache php7.3-cli php7.3-gd php7.3-curl php7.3-mysql
sudo apt install php7.3-fpm php7.3-common php7.3-mysql php7.3-gmp php7.3-curl php7.3-intl php7.3-mbstring php7.3-xmlrpc php7.3-gd php7.3-xml php7.3-cli php7.3-zip php7.3-soap php7.3-imap
php -v

 
sudo systemctl status php7.3-fpm

sudo vi /etc/php/7.3/fpm/php.ini


yum install nginx
systemctl status nginx.service
systemctl start nginx.service

```
