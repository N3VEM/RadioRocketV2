## The Ground Station
The ground station may look impressive, but I promise it's not too complicated!

### Bill of Materials for the Ground Station
* [Libre Computer LePotato Single Board Computer](https://libre.computer/products/aml-s905x-cc/) - Say NO to Fruit Pi!
* [Adafruit Feather 32u4 RFM96 LoRa Radio - 433MHz - RadioFruit](https://www.adafruit.com/product/3079) OR [Adafruit Feather M0 RFM96 LoRa Radio - 433MHz - RadioFruit](https://www.adafruit.com/product/3179)
    * The M0 version is a little more powerful, but either should work fine for you. I used the 32u4 version, only because I already had it from version 1 of this project.    
* [uFL SMT antenna connector for above](https://www.adafruit.com/product/1661)
* [uFL to SMA jumper](https://www.adafruit.com/product/851)
* [SMA RF Jumpers](https://amzn.to/3jMf6Mw)
* [SMA right angle adapters](https://amzn.to/3leU6hK)
* (2) [Antennas](https://amzn.to/3XjlWXB)
* [RTL-SDR Dongle](https://www.rtl-sdr.com/buy-rtl-sdr-dvb-t-dongles/)
* [USB jumper cable for above](https://amzn.to/3Ims2Ct)
* [Battery 'Shoe'](https://amzn.to/3RLUsIW) for the LePotato. I call it a 'shoe' because it goes on the bottom of the board instead of the top, like a traditional 'HAT' would.
* [A pretty power button](https://amzn.to/3ljC0LD)
* Assorted LEDs - colors to your own preferance.
* [Misc. wires and jumpers](https://amzn.to/3jJmsjX). The type used in breadboarding would work fine.
* [Some strip boards](https://amzn.to/3RPnB5S)
* [Micro USB data cables](https://amzn.to/3lr9zv7)
* [USB bulkhead jumper](https://amzn.to/3HS609b) optional, and there are wildly cheaper versions of this - but this is what I used because I had one that was taken out of a peice of commercial equipment.
* RJ45 Bulkhead Connector. The one's I used came out of a peice of commercial equipment, but if you search you'll find lots of options.
* [standoffs](https://www.adafruit.com/product/3299)
* [12/24v to 5v DC-DC Converter](https://amzn.to/3YBZTMW)
* [Barrel Jack](https://amzn.to/3DXKkHn)
* Zip Ties, Zip Tie Mounts
* [Enclosure](https://amzn.to/3HPVTBr)

### Physical Construction
I have 4 kids, so I probably won't find time to do a step by step.  Build to suit, refer to pictures in this folder for inspiration, and feel free to contact me if you have specific questions :-)

### Software
In Progress...

Download Armbian CLI Image from [here](https://www.armbian.com/lepotato/)  

Burn to SD Card, install in LePotato, connect to network, and boot it up.

Follow the initial steps on first boot to update passwords, create users etc.

[install direwolf](https://github.com/wb2osz/direwolf#linux---using-git-clone-recommended)

```sudo apt install pkg-config```  

Install RTL-SDR command line tools using [these directions](https://github.com/wb2osz/direwolf/blob/master/doc/Raspberry-Pi-SDR-IGate.pdf)
this will fail with errors if you don't install pkg-config first.  

install [node red](https://nodered.org/docs/getting-started/raspberrypi)  

edit your crontab:  
```sudo crontab -e```  
and then add these lines which will start the rtl dongle, direwolf, and turn on the attached LEDs to indicate stuff is working
```
@reboot sleep 30 && rtl_fm -f 144.39M - | direwolf -c sdr.conf -r 24000 -D 1 - 
@reboot sudo gpioset 1 83=1
* * * * * systemctl is-active --quiet nodered && sudo gpioset 1 84=1; systemctl is-active --quiet nodered || sudo gpioset 1 84=0
```

import the flow located here in the folder,into node red.

via node red pallete, you'll need to add:
node-red-contrib-mastodon
node-red-contrib-ui-led
node-red-dashboard
node-red-node-serialport
node-red-node-smooth

There will be some other errors to resolve probably - ping me on mastodon, or I'm good on QRZ and I can help you out.

