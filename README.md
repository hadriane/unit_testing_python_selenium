## Frontend Unit Testing Python App With Selenium

### Tools

|            | Tools |         |
|------------|:-----:|:-------:|
|  Selenium  | Flask |  MySql  |
| Python 3.6 | Xvfb  |         |

### Platform

- Platform : AWS
- Operating System : CentOS Linux release 7.7.1908 (Core)
- AMI ID : ami-02eac2c0129f6376b

### Overview of Steps

**[Flask App Server](https://github.com/hadriane/unit_testing_python_selenium/edit/master/steps/flask_app_server.md)**
1) Install Python and MySQl
2) Enable and start MariaDB
3) Create MariaDB database, user and table
4) Install Flask and its dependancies
5) Make a directory for the Flask app
> ***Aternatively** run this [script](https://github.com/hadriane/scripts/edit/master/installation/flask_app.sh) on the server to do an automatic installation*
6) Download the Flask app files from [here](https://github.com/hadriane/scripts/tree/master/app/flask) to /opt/flaskapp
7) Move into /opt/flaskapp and start the Flask dev server
8) Check if you can access the webpage


**[Selenium Server](https://github.com/hadriane/unit_testing_python_selenium/blob/master/steps/selenium_server.md)**
1) Install Python 3, wget and bzip2
2) Install headless dependancies
3) Install Selenium
4) Install PhantomJS
5) Launch an XWindows
6) Instruct XWindows to use Xvfb display port
> ***Aternatively** run this [script](https://github.com/hadriane/scripts/blob/master/installation/selenium.sh) on the server to do an automatic installation*
7) To kill the XWindow porcess
    1) Get the process ID
    2) Kill the process

**[Unit Testing](https://github.com/hadriane/unit_testing_python_selenium/blob/master/steps/unit_testing.md)**
1) Download the python Selenium [script](https://github.com/hadriane/scripts/blob/master/unittest/selenium_flaskapp.py) to the Selenium server'
2) Change the IP address in the code to the Flask app server
4) Run the Selenium script
5) Go onto Flask app server
6) Login to MySQL
7) Query the database
