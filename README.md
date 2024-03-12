# ssl-
---
first check apache status running or not
---
check package install for ssl or not(openssl)
--- 
x509 for certificate
commnd for ssl certificate generation
---
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/ssl/private/example.key -out /etc/ssl/certs/example.crt
---
after running this command provide details if you want to 
---
change directory 
cd /etc/apache2/sites-available
check default ssl conf    ---
SSLEngine on
SSLCertificateFile      /etc/ssl/certs/example.crt
                SSLCertificateKeyFile /etc/ssl/private/example.key
 ---
 for enabling this certificate
 a2ensite default-ssl.conf
 ---
 enable sslcertificate module
 sudo a2enmod ssl
  
 check config
 --- apache2 -t (if error check config file and reload apache and restart)
 systemctl reload apache2
 systemctl restart apache2
 ---
 https://65.0.97.225/ check your data
 ---
 for certbot verified secure certificate check details from the given link
 ---
 https://www.digitalocean.com/community/tutorials/how-to-secure-apache-with-let-s-encrypt-on-ubuntu-20-04
 

