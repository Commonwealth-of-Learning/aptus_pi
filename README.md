# Aptus Pi - Assembly Instructions

### Hardware
* Raspberry Pi 4 Model B board: https://www.raspberrypi.org/products/raspberry-pi-4-model-b/
* Class 10 Micro SD card: https://www.amazon.ca/b/ref=dp_bc_aui_C_5?ie=UTF8&node=3381334011
* Case: https://thepihut.com/collections/raspberry-pi-cases
* Power supply: https://www.raspberrypi.org/products/type-c-power-supply/
* Micro SD card reader: https://www.amazon.ca/Anker-Reader-RS-MMC-Support-Warranty/dp/B006T9B6R2 
* Power bank(optional): https://www.powerbankexpert.com/best-raspberry-pi-power-bank/

### Setting up Raspberry Pi
Source: https://projects.raspberrypi.org/en/projects/raspberry-pi-setting-up
1. Download latest Raspberry Pi OS lite: https://www.raspberrypi.org/software/operating-systems/
1. Write to a micro SD card with one of the following tools:
   1. Raspberry Pi Imager:https://www.raspberrypi.org/software/
   1. Win32Diskimager: https://sourceforge.net/projects/win32diskimager/
   1. Etcher: https://www.balena.io/etcher/
1. Insert the micro SD card and boot Raspberry Pi.

### Create a SUDO user account
Source: https://linuxize.com/post/how-to-create-a-sudo-user-on-debian/

Login Raspberry Pi with default username and password: pi/raspberry

Execute the following commands in a terminal:
```console
sudo su
adduser aptus
usermod -aG sudo aptus
```
### Enable SSH
Source: https://www.raspberrypi.org/documentation/remote-access/ssh/

Launch raspi-config by entering the following command in a terminal:
```console
sudo raspi-config
```
* Select Interfacing Options
* Navigate to and select SSH
* Choose Yes
* Select Ok
* Choose Finish

Alternatively, use systemctl to start the service
```console
sudo systemctl enable ssh
sudo systemctl start ssh
```

### WiFi Hotspot and DNS
Source: https://github.com/RaspAP/raspap-webgui

Set the WiFi country in raspi-config's Localisation Options
```console
sudo raspi-config
```



### Captive Portal (optional)
Source:https://www.maketecheasier.com/turn-raspberry-pi-captive-portal-wi%E2%80%90fi-access-point/

### Web Administration Portal(optional)
Source: https://pimylifeup.com/raspberry-pi-webmin/





