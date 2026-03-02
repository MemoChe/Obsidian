To install apache on Fedora it is as simple as  
`sudo dnf install httpd` and then start our server in `sudo systemctl start httpd.service`. Fedora has similar paths to arch linux, however there is another default folder that `/srv/http/`, now the default folder is in `/var/www/html/`. If we are in other distributions we can realize that in the configuration file that is in `/etc/httpd/conf/httpd.conf` is the parameter DocumentRoot where it indicates the folder to upload our files.

/etc/httpd/conf/httpd.conf => configuration file
Parameter DocumentRoot => Path to upload files
Parameter User/Group => Path to define the user with his group.

ARCH LINUX LAMP
APACHE PACKAGES
The main Apache configuration file is located at /etc/httpd/conf/httpd.conf and the default Document Root is /srv/http that is where we will put our projects
`sudo pacman -S apache`
`sudo systemctl start httpd.service`
`sudo chmod -r 777 /srv/http`

PHP PACKAGES
`sudo pacman -S php php-apache`
The main PHP configuration file is well-documented and located at /etc/php/php.ini
I should want display error in browser set in the php.ini: display_errors = On
If we want to use Mysql operations in our php scripts to connect to a Mysql database, uncomment these lines in php.ini
extension=mysqli    extension=pdo_mysql
By default Apache would just server your php files as plain text files. To make apache execute your php scripts follow these steps.
Make sure that mpm_event module is disabled and the mpm_prefork module is enabled:
```
#LoadModule mpm_event_module modules/mod_mpm_event.so
LoadModule mpm_prefork_module modules/mod_mpm_prefork.so
```

Now we will enable PHP module, add to your httpd.conf:
```
LoadModule php_module modules/libphp.so
AddHandler php-script .php
Include	conf/extra/php_module.conf
```

MARIADB PACKAGES
`sudo pacman -S mariadb`
Config Mariadb
`mariadb-install-db --user=mysql --basedir=/usr --datadir=/var/lib/mysql`
`sudo systemctl start mariadb.service`
`sudo mysql_secure_installation`
`mysql -u root -p`
and we put yes to everything 


