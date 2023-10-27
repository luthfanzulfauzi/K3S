### Install MYSQL

Install MYSQL and enable service
```
dnf module list mysql
dnf module enable mysql:8.0
dnf install @mysql
systemctl enable mysqld
systemctl start mysqld
systemctl status mysqld
```

Configure Mysql- and initialize password
```
mysql_secure_installation
```

Login to mysql
```
mysql -uroot -p
```

Create new user for K3S
```
create user 'username'@'allowedip' identified by 'yourpassword';
create user 'k3s'@'10.%' identified by '8YyFTdgkG8sCYH_WW';
grant create, select, insert, delete, update on *.* to 'k3s'@'10.%';
```