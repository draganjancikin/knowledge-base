# MySQL

```bach
sudo mysql -u root

mysql> USE mysql;
mysql> SELECT User, Host, plugin FROM mysql.user;

mysql> UPDATE user SET plugin='mysql_native_password' WHERE User='root';
mysql> FLUSH PRIVILEGES;
mysql> exit;

service mysql restart
```
