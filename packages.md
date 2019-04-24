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

### Install PHP
```bash
sudo apt-get install php libapache2-mod-php
```
###### Install Redis PHP Extension
```bash
sudo apt-get install php-redis
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
