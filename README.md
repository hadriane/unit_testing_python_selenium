## Frontend Unit Testing Python App With Selenium

### Tools

|          | Tools |         |
|----------|:-----:|:-------:|
| Selenium | Flask |  MySql  |
| Firefox  | Xvfb  | Firefox |

### Platform

- Platform : AWS
- Operating System : CentOS Linux release 7.7.1908 (Core)
- AMI ID : ami-02eac2c0129f6376b
- Python Version : 3.6.8

### Overview of Steps

**[Flask App Server]()**

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
2) Change the IP address in the code accordingly
4) Run the Selenium script
5) Go onto Flask app server
6) Login to MySQL
7) Query the database
