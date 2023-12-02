


###  Setup mail-server in ubuntu 22.04

```
https://youtu.be/jaZx-k4QmbU?si=hXp_S4GAkPMxRUoZ 

# Update package information
sudo apt update

# Install Postfix
sudo apt-get install -y postfix

# Edit the Postfix configuration file
sudo nano /etc/postfix/main.cf

# Add the following line to the configuration file
myhostname = keenable.com

# Save the changes and exit the editor

# Restart Postfix service
sudo service postfix restart

# Check the status of the Postfix service
sudo service postfix status

# Install mailutils
sudo apt-get install -y mailutils

# Create user1
sudo su
sudo adduser user1
sudo passwd user1
# Enter password: rahul
# Confirm password: rahul

# Create user2
sudo useradd user2
sudo passwd user2
# Enter password: rahul
# Confirm password: rahul

# Send a test email to user1
echo "Hi, this is a test" | mail -s "Test Email" user1

# Switch to user1
su user1

# Install Dovecot
sudo apt-get install -y dovecot-core dovecot-imapd dovecot-pop3d

# Install Apache
sudo apt-get install -y apache2

# Add PHP repository
sudo add-apt-repository ppa:ondrej/php -y
sudo apt-get update

# Install PHP 7.4
sudo apt-get install -y php7.4

https://sourceforge.net/projects/squirrelmail/files/stable/1.4.22/squirrelmail-webmail-1.4.22.tar.gz/download?use_mirror=webwerks  





sudo scp squirrelmail-webmail-1.4.22.tar.gz ldap-client@192.168.122.123:/home/ldap-client/







# Extract the SquirrelMail archive
tar -zxvf squirrelmail-webmail-1.4.22.tar.gz

# Move the extracted files to the web server directory
sudo mv squirrelmail-webmail-1.4.22 /var/www/html

# Set ownership of the SquirrelMail directory to the web server user
sudo chown -R www-data:www-data /var/www/html/squirrelmail-webmail-1.4.22

# Set the correct permissions for the SquirrelMail directory
sudo chmod -R 755 /var/www/html/squirrelmail-webmail-1.4.22

# Rename the SquirrelMail directory for simplicity
sudo mv /var/www/html/squirrelmail-webmail-1.4.22 /var/www/html/squirrelmail


sudo perl /var/www/html/squirrelmail/config/conf.pl

2







tar -zxvf squirrelmail-webmail-1.4.22.tar.gz



sudo mv squirrelmail-webmail-1.4.22. /var/www/html


sudo chown -R www-data:www-data /var/www/html/squirrelmail-webmail-1.4.22


sudo chown 755 -R /var/www/html/squirrelmail-webmail-1.4.22

sudo mv /var/www/html/squirrelmail-webmail-1.4.22 /var/www/html/squirrelmail

sudo perl /var/www/html/squirrelmail/config/conf.pl


http://192.168.122.123/squirrelmail/src/webmail.php 


```




