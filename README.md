# Cac ghi chep ve PHPIPAM


THAM KHAO

http://frankhinek.com/how-to-setup-phpipam-on-ubuntu-14-04/

sudo apt-get update
sudo apt-get -y install apache2 mysql-server php5 php5-gmp php-pear php5-mysql php5-ldap wget

- Tai bo cai phpipam o dia chi duoi, sau do dung winscp copy vao thu muc root
https://sourceforge.net/projects/phpipam/

- Giai nen 
tar -xvf phpipam-1.2.1.tar -C /var/www


- Cau hinh apache2

a2dissite 000-default.conf
a2enmod rewrite
service apache2 restart

cp /etc/apache2/sites-available/000-default.conf /etc/apache2/sites-available/ipam.conf

- Mo file /etc/apache2/sites-available/ipam.conf bang vi

vi /etc/apache2/sites-available/ipam.conf

- Sua cac dong sau

ServerName ten_may_chu

DocumentRoot /var/www/phpipam

- Kich hoat virtalhost cho ipam

a2ensite ipam.conf
service apache2 reload

- Cau hinh IPAM

vim /var/www/phpipam/config.php


