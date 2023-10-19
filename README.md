# UNIHIKER Setup

## Getting Started with UNIHIKER

Please read the following official guide first (UNIHIKER guide from DFRobot):
[Getting Started with UNIHIKER](https://www.unihiker.com/wiki/get-started)

### 0. Connect to UNIHIKER Device Using `ssh`

Connect UNIHIKER using USB-C cable to your laptop, access via ssh into it:

* IP Address: 10.1.2.3
* Username: root
* Password: dfrobot
* Port: 22

    ssh root@10.1.2.3


### 1. Change The Default `root` Password

    passwd

### 2. Change The Default TimeZone

I live in Cimahi, West Java - Indonesia; I set the Time Zone to Asia/Jakarta (+0700)

    timedatectl
    timedatectl set-timezone Asia/Jakarta
    timedatectl

### 3. Check The Linux OS Version

    uname -a
    cat /etc/os-release

![UNIHIKER Linux OS version](https://raw.githubusercontent.com/danito-net/UNIHIKER-Setup/main/images/unihiker-linux-os-version.png)

Image file: [unihiker_v0.3.5-202304.img.7z](https://download3.dfrobot.com.cn/unihiker/img/unihiker_v0.3.5-202304.img.7z)
Please reffer to this [official tutorial for burning the image file](https://www.unihiker.com/wiki/burner).

### 4. Update and Upgrade

    apt update
    apt upgrade


### 5. Install New Version of Python3

UNIHIKER using Python3.7 as a default

![UNIHIKER Python versions](https://raw.githubusercontent.com/danito-net/UNIHIKER-Setup/main/images/unihiker-python-versions.png)

Let's install a newer one (Python 3.10.13)

     wget https://www.python.org/ftp/python/3.10.13/Python-3.10.13.tgz
     tar xvzf Python-3.10.13.tgz
     cd Python-3.10.13
     ./configure --enable-optimizations
     make
     make altinstall
     cd /usr/bin/
     rm python
     ln -s /usr/local/bin/python3.10 python
     rm python3
     ln -s /usr/local/bin/python3.10 python3
     
![Python version 3.10.13](https://raw.githubusercontent.com/danito-net/UNIHIKER-Setup/main/images/unihiker-python-version3.10.13.png)

