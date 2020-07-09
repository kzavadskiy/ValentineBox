# ValentineBox
Arduino project of gift box for Valentines day
![Foto](https://raw.githubusercontent.com/kzavadskiy/ValentineBox/master/IMG_20200523_154603.jpg)

Переклад українською [тут](https://github.com/kzavadskiy/ValentineBox/blob/master/README.ua.md)

This small project will allow you to give a good mood and surprise your partner not only on Valentine's Day, but also on other important dates for you.

The project was created on the idea of Vegard Paulsen, link [here](https://vegardpaulsen.wordpress.com/valentineduino/)

List of required components:
* Arduino Nano ~ 3 usd
* RTC module DS3231 with 2032 battery ~ 1.4 usd
* 4 digits, 3-segment display ~ 1.8 usd
* 220 ohm resistors, 6 pieces <1 usd
* mounting wire
* old USB cable
* any box
* tools

The wiring diagram can be assembled according to Figure 1 by hinged mounting or on a circuit board. It is possible both to solder conductors, and to use assembly conductors, it is desirable to connect on the DS3231 module contacts SCA, SCL through assembly conductors, with a possibility of convenient disconnection.

![Scheme](https://raw.githubusercontent.com/kzavadskiy/ValentineBox/master/Schematic_Valentine%20Box.png)

Figure 1. Wiring diagram ValentineBox

Connect the 5V, GND contacts to the appropriate wires of the USB cable

## Sketch

SevSeg, Wire, DS3231 libraries must be installed for the modules to work properly.

First of all, you need to configure the real-time module. After assembling the circuit, you need to fill in the sketch [Setting time](https://github.com/kzavadskiy/ValentineBox/blob/master/Setting%20time) on Arduino nano with installed battery in module DS3231. 

After that, you can fill the main [sketch] (https://github.com/kzavadskiy/ValentineBox/blob/master/box_sketch) with disconnected contacts SCA, SCL.

The variable dateWeGotTogether must record your memorable date in unixtime format. To do this, use the date converter https://www.unixtimestamp.com/index.php

After checking the operation, you can assemble the box, when the power is off, the real-time module saves the date and time, and after connecting to the power supply via USB cable, the date remains relevant.

  



