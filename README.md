# host-php-website-  contains [mysql server,php ,php database app] chinal name wap institute
-- * Used Commands *--
#1. update apt
sudo apt-get update

#2. install mysql
sudo apt-get install mysql-server

#3. mysql secure installation
sudo mysql_secure_installation

#4. install apache
sudo apt-get install apache2

#5. install php
sudo apt-get install php libapache2-mod-php

#6. restart apache
sudo systemctl restart apache2

#7. install phpmyadmin
sudo apt-get install phpmyadmin php-mbstring php-gettext

#8. fix if php myadmin not work
sudo ln -s /etc/phpmyadmin/apache.conf /etc/apache2/conf-available/phpmyadmin.conf
sudo a2enconf phpmyadmin.conf
sudo systemctl restart apache2

#9. enable file permission
sudo chown ubuntu /var/www/html

#10. change phpmyadmin password
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'new_password';


#FOR ssl certificates on command line geerate 
sudo add-apt-repository ppa:certbot-apache
sudo apt0get update
sudo apt-get install python-certbot-apache
certibot --apache -d abhijitramteke.site 

then enter and ok and choose 
