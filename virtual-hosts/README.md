# Virtual Hosts

Prerequisites: PHP, MySQL and Apache2

Check version:

```bash
php -v
mysql -V
apache2 -v
```

## Step 1: Make folder

```bash
# argument -p means, make parent directories as needed
sudo mkdir -p /var/www/naziv_sajta/web
```

## Step 2: Change files permissions

```bash
sudo chown -R $USER:$USER /var/www/naziv_sajta/web
sudo chmod -R 755 /var/www
sudo chmod 777 /var/www/naziv_sajta
```

## Step 3: Create virtual host

```bash
sudo cp /etc/apache2/sites-available/000-default.conf /etc/apache2/sites-available/naziv_sajta.conf
```

## Step 4: Edit naziv_sajta.conf

```bach
sudo gedit /etc/apache2/sites-available/naziv_sajta.conf
```

```php
# add code
<VirtualHost *:80>
    ServerAdmin admin@example.com
    ServerName naziv_sajta
    ServerAlias www.naziv_sajta
    DocumentRoot /var/www/naziv_sajta/web
    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```

## Step 5: Add host to /etc/hosts

```bash
sudo gedit /etc/hosts
```

```php
# add code
```

## Step 6: Host activation

```bash
sudo a2ensite naziv_sajta.conf
```

## Step 7: Apache restart

```bash
systemctl reload apache2
```

## Step 8: Check virtual hosts

```bash
apache2ctl -S
```
