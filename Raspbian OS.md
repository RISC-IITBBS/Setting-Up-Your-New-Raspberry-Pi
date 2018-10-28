# Raspbian OS - OS for Raspberry Pi
- Download at https://www.raspberrypi.org/downloads/raspbian/
- The above link has 2 types of Raspbian OS
  - Raspbian With Desktop
  - Raspbian Lite.


### Raspbian with Desktop
- Contains GUI

### Raspbian Lite
- Contains minimal OS with no GUI and only CLI (command line interface)
- To get a GUI (lightdm display manager) for this, run the following commands in the Raspberry Pi Terminal:
```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install raspberrypi-ui-mods
sudo apt-get install lightdm
lightdm
reboot
```

### Making a Bootable SD Card
- In Windows, you can make a bootable SD Card using Rufus https://rufus.ie/en_IE.html
- In Ubuntu, you can make a bootable SD Card using the pre-installed Startup Disk Creator application. Refer tutorial at https://tutorials.ubuntu.com/tutorial/tutorial-create-a-usb-stick-on-ubuntu#5
- The SD Card should have space enough to accomodate the OS or more
- The SD Card chosen will be formatted and the OS will be it only contents

### Booting the Raspberry Pi for the first time
- Carefully insert the bootable SD Card without powering up the Raspberry Pi (If the Raspberry Pi is powered on, nothing happens and displays a blank screen on the connected display)
- Connect peripherals like 
  - Monitor Display via HDMI
  - Mouse and Keyboard via USB
  - RJ45 Lan Cable at the Internet Lan Port as per requirements
- Turn on the Raspberry Pi by powering it via a Micro USB Power Adapter (5V / 1~2A)
