# Koha-24.05-Installation (Debian & Debian-based Linux Distributions)

## Step-by-step Process
1. sudo apt-get update
2. sudo apt-get upgrade
3. echo 'deb https://debian.koha-community.org/koha stable main' | sudo tee /etc/apt/sources.list.d/koha.list
4. wget -O- https://debian.koha-community.org/koha/gpg.asc | sudo apt-key add -
5. sudo apt-get update
6. sudo apt-get install koha-common
7. sudo nano /etc/koha/koha-sites.conf
8. sudo apt-get install mysql-server
9. sudo a2enmod rewrite
10. sudo a2enmod cgi
11. systemctl restart apache2
12. sudo koha-create --create-db library
12. sudo nano /etc/apache2/ports.conf
13. sudo service apache2 restart
14. sudo a2dissite 000-default
15. sudo a2enmod deflate
16. sudo a2ensite library
17. sudo service apache2 restart
18. sudo koha-passwd library
