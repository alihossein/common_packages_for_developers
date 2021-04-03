#### Install openvpn
#### run : sudo openvpn --config /path/to/config.ovpn
```
sudo apt-get install openvpn
```

## Install Maven
```
sudo apt-get install maven
```


## Install Maven 3.6.3 (manually)
```
wget https://www-us.apache.org/dist/maven/maven-3/3.6.3/binaries/apache-maven-3.6.3-bin.tar.gz -P /tmp
sudo tar xf /tmp/apache-maven-*.tar.gz -C /opt
sudo ln -s /opt/apache-maven-3.6.3 /opt/maven 

# find java home
readlink -f /usr/bin/java

vim /etc/profile.d/maven.sh
export JAVA_HOME=/usr/lib/jvm/default-java
export M2_HOME=/opt/maven
export MAVEN_HOME=/opt/maven
export PATH=${M2_HOME}/bin:${PATH}


sudo chmod +x /etc/profile.d/maven.sh
```

## Install Lua 5.4.2
```
sudo apt install build-essential libreadline-dev
curl -R -O http://www.lua.org/ftp/lua-5.4.2.tar.gz
tar -zxf lua-5.4.2.tar.gz
cd lua-5.4.2
make linux test
sudo make install
```

## Install luarocks 3.5
```
wget https://luarocks.org/releases/luarocks-3.5.0.tar.gz
tar zxpf luarocks-3.5.0.tar.gz
cd luarocks-3.5.0
./configure --with-lua-include=/usr/local/include
make
sudo make install
```

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
