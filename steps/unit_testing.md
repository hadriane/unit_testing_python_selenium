**Unit Testing The Flask App**

1) Download the python Selenium [script](https://github.com/hadriane/scripts/blob/master/unittest/selenium_flaskapp.py) to the Selenium server'
2) Change the IP address in the code accordingly
```
driver.get("http://3.234.207.87:5000/")
```
4) Run the Selenium script
```
python3 selenium_flaskapp.py
```
5) Go onto Flask app server
6) Login to MySQL
7) Query the database
```
[root@ip-172-31-3-253 ~]#
[root@ip-172-31-3-253 ~]# mysql -u root

MariaDB [(none)]> use flaskapp;

Database changed
MariaDB [flaskapp]> select * from users;
+------------+---------------------+
| name       | email               |
+------------+---------------------+
| selenium_0 | selenium_0@test.com |
| selenium_1 | selenium_1@test.com |
| selenium_2 | selenium_2@test.com |
| selenium_3 | selenium_3@test.com |
| selenium_4 | selenium_4@test.com |
| selenium_5 | selenium_5@test.com |
+------------+---------------------+
6 rows in set (0.00 sec)

MariaDB [flaskapp]>
```
