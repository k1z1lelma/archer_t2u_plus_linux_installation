# Archer T2U Plus (rtl8812au) Kali Linux İnstallation
TP-Link Archer T2U Plus / AC600 High Gain USB Wifi Adapter Review &amp; Driver installation Guide for Kali Linux.

This adapter has RTL8821AU chipset. The biggest feature of this chipset is that it supports monitor mode. In this way, packet injection can be performed. In addition, the adapter that supports the 5 GHz band should definitely be in your toolbox for penetration tests against current modems.

![adaptor](https://github.com/k1z1lelma/archer_t2u_plus_linux_installation/blob/main/img/tp_link.jpeg)

## Where to buy?

* MediaMarkt
* Teknosa
* Hepsiburada
* Amazon TR

## Driver for Kali Linux / Ubuntu

1) Make the necessary updates
* `sudo apt update`
2) Upgrade the distro. Otherwise you will get an error while installing the dependencies. This process may take some time. (Approximately 15 min.)
* `sudo apt upgrade`
* `apt dist-upgrade`
3) Reboot the system
* `reboot`
4) Install dkms
* `sudo apt install dkms`
5) Install Build Dependencies
* `sudo apt install build-essential libelf-dev linux-headers-$(uname -r)`
* `cd /opt`
6) Download the Driver files using git
* `git clone https://github.com/aircrack-ng/rtl8812au.git`
7) Navigate to the Downloaded directory
* `cd rtl88*`
8) Install the Driver
* `sudo make dkms_install`

9) Check the wireless interfaces by typing `iwconfig`

![iwconfig](https://github.com/k1z1lelma/archer_t2u_plus_linux_installation/blob/main/img/iwconfig.png)
