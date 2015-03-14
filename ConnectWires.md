#How to Connect Wires to cape board

# Connect Wrires #

The cape board has pins for
```
+5 V power
I2C 
ZigBee compatible Uart Socket
PWM input from radio receiver
PWM output to ESC
```

Beaglebone's IO use 3.3 V. There is no voltage converter in cape board. However it seems to be safe to connect to receiver and esc directly.

Power supply is very important for beaglebone. You can use 5V from ESC. However, this is not recommended. Please use a 5V BEC to power beaglebone. Use 2A or more current version. There is 5V connector on cape board for this function.

The current code support gyro itg4200. You can get one from sparkfun or ebay. Connect them with soft thin wire to Cape board. Please make sure the direction is correct if the sensor is mount on cape board.

Receiver can get power from Cape board. Connect Aile, Elev,Rudder and Throttle.

Test the Beaglebone before plug ESCs. The program will running after power on, it will take about 40 seconds to get the ubuntu boot up and get program loadinig. Using a pair of ZigBee module or use [NCD's ZigBee Usb module](http://http://www.controlanything.com/Relay/Device/ZUSB) to connect with computer and run MultiWiiConfig to check if everything works.

All ESC share GND. There are jumpers for get power from ESC. Only one ESC can be used as power.
Front Left
Rear Left
Front Right
Rear Right
The version support X mode only.
Remember remove propellers from motors before make sure everything is correct.
The code is ported from MultiWii project. The way to arm and unarm quad copter is same. Move the rudder to most right and lowest throttle will arm the quad copter. All motors should run at slow speed when armed. Move the rudder to the most left and lowest throttle will unarm the copter.

When quad copter is armed, hold the copter and give it a little bit throttle and try to tilt and roll copter. The copter should try to keep stable if the gyro direction is correct.

Now, you are ready to fly!
