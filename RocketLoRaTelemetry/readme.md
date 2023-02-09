## LoRa and Telemetry in the Rocket

### Bill of Materials for LoRa and Telemetry in the Rocket
Some of the parts quantities here give a range, because the length and quantity of things like jumper wires etc. might change depending on how you lay out your hardware when you build it.

* [PJRC Teensy](https://www.pjrc.com/store/teensy41.html) - I used the version without ethernet, but any of the 4.1 versions should work fine.
* [70cm Adafruit LoRa Breakout](https://www.adafruit.com/product/3073) or if you're not a licensed amature you can use the 900MHz version
* [uFL SMT antenna connector for above](https://www.adafruit.com/product/1661)
* (2) [STEMMA Non-Latching Mini Relay boards](https://www.adafruit.com/product/4409)
* [Adafruit LSM6DSOX + LIS3MDL - Precision 9 DoF IMU - STEMMA QT / Qwiic](https://www.adafruit.com/product/4517)
* [Adafruit APDS9960 Proximity, Light, RGB, and Gesture Sensor - STEMMA QT / Qwiic](https://www.adafruit.com/product/3595)
* [ADXL375 - High G Accelerometer (+-200g) with I2C and SPI - STEMMA QT / Qwiic](https://www.adafruit.com/product/5374)
* [Adafruit BMP390 - Precision Barometric Pressure and Altimeter - STEMMA QT / Qwiic](https://www.adafruit.com/product/4816)
* [Small Enclosed Piezo w/Wires](https://www.adafruit.com/product/1740)
* [Lithium Ion Cylindrical Battery - 3.7v 2200mAh](https://www.adafruit.com/product/1781)
* [Battery Holder](https://amzn.to/3KdAm8X) - remove the metal contacts.
* (3-5) [STEMMA QT / Qwiic JST SH 4-Pin Cable - 50mm Long](https://www.adafruit.com/product/4399)
* (2-3) [STEMMA QT / Qwiic JST SH 4-Pin Cable - 200mm Long](https://www.adafruit.com/product/4401)
* (2-3) [STEMMA JST PH 2mm 3-Pin to Male Header Cable - 200mm](https://www.adafruit.com/product/3893)
* (2-3) [JST PH 2-Pin Cable - Female Connector 100mm](https://www.adafruit.com/product/261)
* (2-3) [JST PH 2-Pin Cable – Male Header 200mm](https://www.adafruit.com/product/3814)
* Protoboard, that you can cut peieces from to the appropriate size. I used some of [these](https://amzn.to/3jPjbj1).
* Misc. [Female Headers](https://amzn.to/3YBBUND) and [Pin Headers](https://amzn.to/3ln0JPa)
* Misc. [M2, M3, M4 hardware](https://amzn.to/3YDgNux)
* Threaded Rod
* Small eye bolts
* Whatever material tickles your fancy for the sled - thin plywood, fiberglass sheets, etc.
* Foil tape.  Make sure to get the actual conductive metal tape, not just silver colored plastic tape. 

### Physical Construction.
More details to come, maybe. I'd like to give step by step directions, but I've got 4 kids and finding time to document this stuff is hard :-) Refer to pictures for reference. Some construction tips below to help you along your way however.

To get the end peices to the correct diamater, use a hole-saw as close in size as you can to make a plug. put a bolt through the middle, clamp the bolt in a drill, and spin the plug against a peice of sandpaper to get it down to size.

For mounting the breakout boards, I used the boards themselves to mark the locations of the mounting points, I then drilled holes into the sled big enough that standoffs would fit inside the hole with their tops sticking out, and I epoxied them into the holes.

### Wiring
Breakout boards follow the standard wiring as described in their respetive Adafrut documents and the pinouts as labled for the PJRC Teensy.  I'll try to add some additional detail on this in the future, but in the meantime feel free to contact me if you need specifics, and I'll use that as the fire under my you-know-what to get that documentation done:-).

For the Teensy and LoRa Breakout, I used the headers and pins to attach them both to piece of strip board, and then used jumper wires on the stripboard useing [The lost are of Strip Board Prototyping](https://www.nutsvolts.com/magazine/article/june2013_Dratwa) to make the interconnections.

Until I get to document the exact wiring, you should also be able to glean it from the Arduino code as the pins used are referenced there.

### The Code
See code files in this folder. Just be certain to edit things there to be your callsign, and not mine :-)  I'm not a software engineer, so the code is mostly bodged together examples, with my additions - after all, this is just for fun! If you think the code sucks, you can either stuff it, or make a pull request :-)

On first compile of the code, you'll get errors telling you which libraries are missing.  You can either go find and install those libraries, or copy the library folders to your computer - it has more than you will need for this project, but should have everything you need.
