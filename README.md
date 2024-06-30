## ssl-
```
first, check whether Apache status is running or not
```
## check whether the package is installed for SSL or not(OpenSSL)
```
openssl version

```
## x509 for certificate
the command for ssl certificate generation with root user or user having sudo power
```
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/ssl/private/example.key -out /etc/ssl/certs/example.crt
```
after running this command provide details if you want to 
```
change directory     cd /etc/apache2/sites-available also add the ssl config to the site config file to enable ssl
```

## Check default ssl conf   
```
SSLEngine on
SSLCertificateFile      /etc/ssl/certs/example.crt
SSLCertificateKeyFile  /etc/ssl/private/example.key
 ```

 ## for enabling this certificate
 a2ensite default-ssl.conf
 ```
 ## enable SSL certificate module
 sudo a2enmod ssl
  
 ## check config
 ```
 apache2 -t (if error check config file reload apache and restart)
 systemctl reload apache2
 systemctl restart apache2
 ```
 https://65.0.97.225/ Check your data
 ```
 ## For certbot verified secure certificate check details from the given link
 ```
 https://www.digitalocean.com/community/tutorials/how-to-secure-apache-with-let-s-encrypt-on-ubuntu-20-04
 

