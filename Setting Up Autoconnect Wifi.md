# Setting Up Connection To Wifi Automatically On Startup
```
sudo nano /etc/network/interfaces
```
add the following code at the end of the file:
```
auto lo

iface lo inet loopback
iface eth0 inet dhcp

auto wlan0
allow-hotplug wlan0

iface wlan0 inet dhcp
    wpa-ssid "your wifi name/ssid"
    wpa-psk "your wifi password"
```
You can also make this change in the SD Card before inserting it into the Raspberry Pi.
Using this, we may not need an HDMI Monitor Display for the first setup.
