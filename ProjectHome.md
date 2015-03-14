## Beagle fly is going to move to support Intel Edison next year! ##

## Cape board version 2 is available now! It is $10 for empty boards without any pins or parts, include shipment inside USA. ##

## Help needed ##
I have the image file for 2G SD card that contains everything. I need a server to host those file as they are pretty big. Please email me if you know where I can get such resource.

## Latest progress ##
I am working on the new cape board. Here are features of new cape board.
### 3 UARTs, one of them has zigbee compatible socket. 2 other has GND and TX/RX line. ###
### Support SPI OLED screen. Have socket for 1.3 inch 1306 based mono oled 128x64 screen. ###
### 4 pin I2c connector and pads for solder directly ###
### 8 Pwm signal for ESC controller. ###
### 6 PPM / PWM signal from receiver. ###
### 2 LEDS ###
### 2 SWITCHES ###
### 8 GPIO ###

I port the program to beaglebone black. It seems extra 300Mhz helps a lot. The quad copter flies very stable!
I will post the steps to make SD card and how to install the program soon!


## What is Beagle-Fly ##
Beagle-Fly is a project to use [BeagleBone ](http://beagleboard.org/Products/BeagleBone) as a flight controller for Quad Copter and other drones.

The project is a open source project.

BeagleBone is a development board from TI. Here are features that make it a great powerful flight controller.

  * Powerful processor that can run linux

  * I2C available on expansion header

  * Serial Port available on expansion header

  * USB Host

  * 2 built PRUs for real time signal processing

![https://sphotos-b.xx.fbcdn.net/hphotos-ash3/p480x480/547858_535489613160194_736625534_n.jpg](https://sphotos-b.xx.fbcdn.net/hphotos-ash3/p480x480/547858_535489613160194_736625534_n.jpg)



It is much easier to develop a program in linux with C/C++ or python than program that runs in chip. Beaglebone runs at 720Mhz. It is fast enough to compile and debug the program just by telnet. The code and data can be transfer with FTP. It is possible to view and config the program from webpage, as ubuntu comes with apache server. It is a full computer!

It has two 0.1 inch 46 pins expansion headers with plenty of GPIO pin. It never been so easy for a linux box talk with sensors, servos and speed controller so easy! PRUSS can hander signal from receiver and control servos or speed controllers without using any main CPU. The data can be accessed through shared memory, which is quick! The gyro, accelerator, compass, and any other i2c devices, can be accessed in linux though i2c bus directly. The board contains everything!

I start this project from port MulitiWii 2.1 to beaglebone. Now I have port the code for Gyro and accelerate. It can be configured by MultiWiiConf. I also made a cape board to make it easier to connect ESC and sensor board. I put the Beaglebone on DJI's F450 frame with Sunnysky 2212 kv 980 motors, 1045 propellers. It flights great!

The next step is port Compass, baro and GPS.

#how to prepare micro SD card

# [Prepare SD card](PrepareSDCard.md) #
# [Connect Wires](ConnectWires.md) #
## Links ##
Here is the link of facebook. https://www.facebook.com/Beaglefly




