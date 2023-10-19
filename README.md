# UNIHIKER Setup

## Getting Started with UNIHIKER

Please read the following official guide first (UNIHIKER guide from DFRobot):
[Getting Started with UNIHIKER](https://www.unihiker.com/wiki/get-started)

Connect UNIHIKER using USB-C cable to your laptop, access via ssh into it:
* IP Address: 10.1.2.3
* Username: root
* Password: dfrobot

    ssh root@10.1.2.3

### 1. Change The Default `root` Password

    passwd

### 2. Change The Default TimeZone

    timedatectl
    timedatectl set-timezone Asia/Jakarta
    timedatectl

### 3. Check The Linux OS Version

    uname -a
    cat /etc/os-release
