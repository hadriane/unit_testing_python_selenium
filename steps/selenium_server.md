### Install and Configure Selenium Server


1) Install Python 3
```
yum -y install python3
```
2) Install Firefox and headless dependancies
```
yum -y install firefox Xvfb libXfont Xorg
yum -y groupinstall "X Window System" "Desktop" "Fonts" "General Purpose Desktop"
```
3) Launch an XWindows
```
Xvfb :99 -ac -screen 0 1280x1024x24 &
```
4) Instruct XWindows to use Xvfb display port
```
export DISPLAY=:99
```
> ***Aternatively** run this [script](https://github.com/hadriane/scripts/blob/master/installation/selenium.sh) on the server to do an automatic installation*
5) To kill the XWindow porcess
    1) Get the process ID
    ```
    [root@ip-172-31-3-115 ~]# ps
    PID TTY          TIME CMD
    1180 pts/0    00:00:00 sudo
    1182 pts/0    00:00:00 su
    1183 pts/0    00:00:00 bash
    2361 pts/0    00:00:00 Xvfb
    2365 pts/0    00:00:00 ps
    [root@ip-172-31-3-115 ~]#
    ```
    2) Kill the process
    ```
    [root@ip-172-31-3-115 ~]# kill 2368
    [root@ip-172-31-3-115 ~]#
    [1]+  Done                    Xvfb :99 -ac -screen 0 1280x1024x24
    [root@ip-172-31-3-115 ~]#
    ```
