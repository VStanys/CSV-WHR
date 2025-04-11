#!/bin/bash
sudo -s 
sudo apt install php8.3-cli 

sudo apt update
sudo apt install apache2 apache2-doc apache2-utils
sudo systemctl start apache2
sudo apt install mysql-server
sudo mysql
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
exit
sudo mysql_secure_installation
sudo apt install php libapache2-mod-php php-mysql
mysql -u root -p
CREATE DATABASE cm4025;
exit
sudo apt install git
git config --global user.name "VStanys" 
cd /var/www/html 
sudo apt update
sudo apt install gh
gh auth login
login to account and generate token 
gh repo clone RobertGordonUniversity/cm4025-coursework-VStanys 
sudo ufw allow ssh
sudo ufw enable
sudo ufw app list
sudo ufw default deny outgoing
sudo ufw allow in "Apache"
sudo ufw allow in "Apache Full"
sudo ufw allow in "Apache Secure"
sudo ufw allow 80/tcp
sudo ufw allow 443/tcp
sudo ufw allow 3306/tcp 
echo ocalhost/cm4025-coursework-VStanys/dbCreate/filldb.php
