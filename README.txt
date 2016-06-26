Web Server Setup for WordPress on debian-ubuntu
=========

1. install unzip,php5-mysqlnd-ms
2. Your script will check if PHP, Mysql & Nginx are installed. If not present, missing packages will be installed.
3. The script will then ask user for domain name. (Suppose user enters example.com)
4. Create a /etc/hosts entry for example.com pointing to localhost IP.


Setup wordpress using wp-cli
========
1. The first thing in creating a virtual host is to a create a directory where we will keep the new website’s information.
2. This location will be your Document Root in the nginx virtual configuration file later on.
3. Download wp-cli and move it to the example.com directory.


3. Download WordPress latest version and unzip it locally in example.com document root.
4. Create wp-config.php,wp database and install wp using wp core install.
5. We need to grant ownership of the directory to the right user, instead of just keeping it on the root system

Changes in php5-fpm
========
We have to make chnges in php5-fpm so that it will listen to the localhost with port 9000.

Changes in nginx
=======
1. Create nginx config file for example.com
2. Remove default file in nginx To both avoid the "conflicting server name error" and ensure that going to your site displays the correct information.

We’ve made a lot of the changes to the configuration. Restart nginx and make the changes visible
Restart nginx and php5-fpm
hit in browser.


