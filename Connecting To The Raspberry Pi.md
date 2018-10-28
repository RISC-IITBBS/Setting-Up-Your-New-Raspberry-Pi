# Connecting To The Raspberry Pi
- HDMI Monitor DIsplay
- Secure SHell (SSH)
- VNC Viewing
- Other Applications/Libraries - refer to their documentations

### HDMI Monitor Display
- Just connect the HDMI Monitor Display and the Raspberry Pi using an HDMI cable and boot up the Raspberry Pi to use it with a GUI

### Secure SHell (SSH)
- Connect the Raspberry Pi and your system to a common network (WiFi/LAN)
- Get the IP of the Raspberry Pi from the network router/access point/third party IP scanner apps
- In you system's terminal type the following command:
  ```
  ssh user@ip
  ```
  User is the username for Raspberry Pi (which is *pi* by default). In my case the command was:
  ```
  ssh pi@192.168.43.42
  ```
  This runs SSH on port 22
- On success you shall be able to access the Raspberry Pi's terminal in your system's terminal like:
  ```
  pi@raspberry $
  ```
- Note that we do not need an HDMI Screen to be connected to the Raspberry Pi for SSH
  
### VNC Viewing
- Install Tight VNC on Raspberry using the following command:
  ```
  sudo apt-get install tightvncserver
  ```
- Set up a password for and run tightvncserver using the following command in the Raspberry Pi's terminal:
  ```
  tightvncserver
  ```
- On setting up the password, the tightvncserver starts running and shows something like:
  ```
  New 'X' desktop is raspberry:2

  Starting applications specified in ...
  Log file is ...
  ```
- On your system, download and install vnc viewer
- Open VNC Viewer
  - Add Computer
  - Type in the IP:590N of Raspberry Pi to connect to it (Where N is the number specified in the tightvncserver output - which is 2 in the above sample output)
  - Use the VNC password set up in the earlier step for authentication
  - On success, the Raspberry Pi GUI pops up
- Note that we do not need an HDMI Screen to be connected to the Raspberry Pi for VNC Vieweing
