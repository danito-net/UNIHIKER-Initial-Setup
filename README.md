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

I live in Cimahi, West Java - Indonesia; I set the Time Zone to Asia/Jakarta (+0700); the default TimeZone is Asia/Shanghai (+0800)

    timedatectl
    timedatectl set-timezone Asia/Jakarta
    timedatectl

![Setting the TimeZone](https://raw.githubusercontent.com/danito-net/UNIHIKER-Setup/main/images/timedatectl-set-timezone-to-asia-jakarta.png)

### 3. Check The Linux OS Version

    uname -a
    cat /etc/os-release

![UNIHIKER Linux OS version](https://raw.githubusercontent.com/danito-net/UNIHIKER-Setup/main/images/unihiker-linux-os-version.png)

This is the default Linux OS version from UNIHIKER's factory. The image file download link for this version here: [unihiker_v0.3.5-202304.img.7z](https://download3.dfrobot.com.cn/unihiker/img/unihiker_v0.3.5-202304.img.7z)
Please reffer to this [official tutorial for burning the image file](https://www.unihiker.com/wiki/burner).

### 4. Update and Upgrade

    apt update
    apt upgrade


### 5. Install `neofetch`

    apt install neofetch
    neofetch

![UNIHIKER neofetch output](https://raw.githubusercontent.com/danito-net/UNIHIKER-Setup/main/images/unihiker-neofetch.png)

### 6. Install `libssl-dev` and `lzma` (for Python 3.8 compiling requirements)<img width="778" alt="default-unihiker-python3-version" src="https://github.com/danito-net/UNIHIKER-Setup/assets/2394242/2b5b403d-5c76-4770-ae5c-15b39f04839e">

UNIHIKER using Python version 3.7.3 as a default Python installation
![UNIHIKER default Python version](https://raw.githubusercontent.com/danito-net/UNIHIKER-Setup/main/images/default-unihiker-python3-version.png)

If you wan't to compile the newer version, please do this following steps:

    apt install libssl-dev lzma

