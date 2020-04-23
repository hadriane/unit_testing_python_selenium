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
1) Install Python 3
2) Install Firefox and headless dependancies
3) Launch an XWindows
4) Instruct XWindows to use Xvfb display port
> ***Aternatively** run this [script](https://github.com/hadriane/scripts/blob/master/installation/selenium.sh) on the server to do an automatic installation*
5) To kill the XWindow porcess
    1) Get the process ID
    2) Kill the process
