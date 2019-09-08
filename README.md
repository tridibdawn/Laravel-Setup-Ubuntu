# laravel-setup
```
setting up laravel
```

# Initialize laravel Project
```
composer create-project --prefer-dist laravel/laravel blog
```

# Setting up hosts
```
sudo gedit /etc/hosts
```

Add this line at end
> 127.0.0.1 laratest.test

# Setting up 000-default.conf
> sudo gedit /etc/apache2/sites-available/000-default.conf

# Add the followings at end:
```
  <VirtualHost *:80>
        DocumentRoot /var/www/html/laratest/public
       	ServerName laratest.test

   <Directory /var/www/html/laratest/public/>
       		    AllowOverride All
   </Directory>
        
        ErrorLog ${APACHE_LOG_DIR}/error.log
        CustomLog ${APACHE_LOG_DIR}/access.log combined
  </VirtualHost>
```
