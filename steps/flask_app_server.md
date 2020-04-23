### Install and Configure Flask App Server

1) Install Python and MySQl
```
yum -y install python3 python3-devel.x86_64 mysql-devel gcc-c++.x86_64 mariadb-server
```
2) Enable and start MariaDB
```
systemctl enable mariadb
systemctl start mariadb
```
3) Create MariaDB database, user and table
```
mysql -e "DROP USER ''@'localhost'"
mysql -e "DROP USER ''@'$(hostname)'"
mysql -e "FLUSH PRIVILEGES"
mysql -e "CREATE DATABASE flaskapp"
mysql -e "CREATE USER 'flaskapp'@'%' IDENTIFIED BY 'StaySafe'"
mysql -e "GRANT ALL PRIVILEGES ON flaskapp.* TO 'flaskapp'@'%' IDENTIFIED BY 'StaySafe'"
mysql -e "FLUSH PRIVILEGES"
mysql -e "USE flaskapp; CREATE TABLE users(name varchar(20), email varchar(40))"
mysql -e "UPDATE mysql.user SET Password = PASSWORD('StaySafe') WHERE User = 'root'"
```
4) Install Flask
```
pip3 install Flask
```
5) Make a directory for the Flask app
```
mkdir /opt/flaskapp
```
6) Download the Flask app from [here](https://github.com/hadriane/scripts/tree/master/app/flask) files to /opt/flaskapp
6) 
