# Bus Shelter
Creates the Display for the Bus Shelter with a map that displays bus location in real time and a bus schedule for different routes. 


## Installation Instructions for Raspberry Pi
Update the software, install the necessary programs, and reboot the Raspberry Pi. 

```bash
sudo apt update
sudo apt upgrade
sudo apt install iceweasel git xscreensaver
sudo shutdown -r now
```

Change the screen orientation to portriat if in landscape by editing /boot/config.txt.
```bash
sudo nano /boot/config.txt
```
Add the following line to the the end of the file.
```bash
display_rotate=1
```

Turn the screensaver off by clicking the menu button in the top left corner, clicking preferences, and clicking screensaver. In the display modes tab, click disable screensaver under the mode dropdown list. Close the screensaver preferences window. 

Change the default password on the raspberry pi and allocate 128M of memory to the gpu through raspi-config. Reboot the Raspberry Pi.
```bash
sudo raspi-config
sudo shutdown -r now
```

Clone the repository, install the HideScrollbars extension, and open bus-shelter.html in Firefox.
```bash
git clone https://github.com/gwokin/Bus-Shelter.git
sudo firefox -install-global-extension addon-494068-latest.xpi
firefox Bus-Shelter/bus-shelter.html &
```

The following url ([http://egauge34.egaug.es/](http://egauge34.egaug.es/)) in the bus-shelter.html file will need to be changed to the web address for our current EGauge EG3000 monitoring system. Right now it points to a public egauge monitoring system and not to our current system. 

Press F11 in Firefox to enable full screen and the display should be good to go!
