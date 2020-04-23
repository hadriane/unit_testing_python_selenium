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
4) Install Flask and its dependancies
```
pip3 install Flask pyyaml flask_mysqldb
```
5) Make a directory for the Flask app
```
mkdir /opt/flaskapp
```
6) Download the Flask app from [here](https://github.com/hadriane/scripts/tree/master/app/flask) files to /opt/flaskapp
7) Move into /opt/flaskapp and start the Flask dev server
```
[root@ip-172-31-3-22 ~]# cd /opt/flaskapp/
[root@ip-172-31-3-22 flaskapp]# python3 app.py
app.py:7: YAMLLoadWarning: calling yaml.load() without Loader=... is deprecated, as the default Loader is unsafe. Please read https://msg.pyyaml.org/load for full details.
  db = yaml.load(open('db.yaml'))
 * Serving Flask app "app" (lazy loading)
 * Environment: production
   WARNING: This is a development server. Do not use it in a production deployment.
   Use a production WSGI server instead.
 * Debug mode: on
 * Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)
 * Restarting with stat
/opt/flaskapp/app.py:7: YAMLLoadWarning: calling yaml.load() without Loader=... is deprecated, as the default Loader is unsafe. Please read https://msg.pyyaml.org/load for full details.
  db = yaml.load(open('db.yaml'))
 * Debugger is active!
 * Debugger PIN: 210-114-020
```
8) Check if you can access the webpage by opening up http://<public_ip_of_flask_server>:5000 in a web browser
![flask_app](https://github.com/hadriane/unit_testing_python_selenium/blob/master/images/flask_app.png)
