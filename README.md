#!/bin/bash

#php
sudo apt install php8.3-cli 
sudo apt update
#apache
sudo apt install apache2 apache2-doc apache2-utils
sudo systemctl start apache2
#mysql
sudo apt install mysql-server
echo Copy this - ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password'; - exit
sudo mysql
echo mysql root password is password
#database
echo Copy this - CREATE DATABASE cm4025;
mysql -u root -p
sudo mysql_secure_installation
sudo apt install php libapache2-mod-php php-mysql
#git
sudo apt install git
cd /var/www/html 
sudo apt update
#github
sudo apt install gh
#firewall
sudo ufw allow ssh
sudo ufw enable
sudo ufw default deny outgoing
sudo ufw allow in "Apache"
sudo ufw allow in "Apache Full"
sudo ufw allow in "Apache Secure"
#ports for database and mysql
sudo ufw allow 80/tcp
sudo ufw allow 443/tcp
sudo ufw allow 3306/tcp 



#Manual
gh auth login
gh repo clone RobertGordonUniversity/cm4025-coursework-VStanys 
echo website link to create DB - localhost/cm4025-coursework-VStanys/dbCreate/filldb.php
sudo ufw enable
