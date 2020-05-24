# ValentineBox
Arduino project of gift box for Valentines day
![Foto](https://lh3.googleusercontent.com/zsYO3oxreWbP0d8SufO2Wx7JvZOUeQSrICO7VNHVK3ys23LzPO-s1nXEhfPwgTgUEKrC0hyDTvxF-3sO7x4S691Ke4ylLM8sJr7Ne8aTJthsNc81nhdhf8s9GH9rGcMVUOiH3igOYbIzAw1fMrclcBwpNpQAblWZy3Pp3jSs_9DnBToHs1uo6fTz-AIRNu-RrJ0nZb0NPnOqqqM-jXApjLhGEe18rzNunjHX6rvrM716FCsjxgBd4wcOL-Q82-O2g551veDFHm2N5KnhMLesH9CYmf3Go1i8E3bzgY2C5IHdmumoO8b9YkOHT9US40BuKZbfNBFHyoc_ABPfHa2PqIHeCEgAUCnvThzJMrvcUVZymOkQ-wWGErG-WP66DnMGEeP5VIo0GXGXrYURLxGIZrFjkpGQwE8Nk8LzJYodQQEAzhR-DjLhvaolCp1HrztInszEYt0PBR52vZqhm6_2Bb5j1jNeTCPn-3WNWQwpf6b_xLfs42UliupfYjhPnJa9Q07ZrGpWQNWL8pqaxsAZiSYlMiSF4OmLW75r7MiRpJXZ78p0B2JRz8QZisCTSEYGZ8XqpAa69RcpPW_h9TXsvvmcvKtj-532DkzIrtIsLrX8AZba5SPQK8UfmIIXff3KJdMVq_Y2MjGIK7QzQl-eqOLZ6wSyHIpOxjMHekZvQl2rCAVRvoCGbjc3eJ9Y=w872-h654-no?authuser=0)

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

![Scheme](https://lh3.googleusercontent.com/C0eLP7MX9KyfVlWX35nVtFYSX55kJ22HcbiFyaYtI_rm8lAYkZcHnOkICZqad9HaUam8NfuwUAVjqO48W2DQj-pkv85jCPJvbpT7W6Qg7Tj8MSITcDHqRMryfY_eHac_YRIv-Oy2UQv7rWjDXUFiM2pz8owH3e5oUUHp43EFb9-rELdk0tUR5aUznW0FO6bk3Xf4zUbzvm6gz80FCR12D0iVVPZ9S0mLQWtqY-D7Rz6Jxdm_LJy-2X6DviY7h5zg7Ufg8VRsVBOf_RlrexeZ6CFodxbMEzfj3QHVB4Rd-JNQ0cNW8a6XPzg0Dzr9UXp4R4bLBzEI-or1UqK8Rfq00BRjKGWUr_F7Yv-cfARKgg-XfyJKodtBulrP_lng5N75rfd8PbF-XtHnvnIMbgkUh89tv78EtcRSo6A7w95w8sRs3pzlGHRdhIx60CF-0-8MBc1OARfK5GAa-nYwPc3Rh8_B_C-xkWGB8VMnPo3i3xfx0bUVaDRgTgSVPiXdALVXd0I_0_zvux0mIzDrGZg_mGnNjLCrmoyazkCnWaCzFjWjLBKS_u5P82TwE08QRg_qxIxuh1XaXOHJ_Oqk7WLCv4SorvL8ehwAgsGT_eDmSOqH0GpRP8I-xoaN0UCuTeBbyLtudAOUqkLv035ukw6jBNUV--kX1a0o2svUg4Ipn940jdMf9fFWFQ05Np-z=w857-h436-no?authuser=0)

Figure 1. Wiring diagram ValentineBox

Connect the 5V, GND contacts to the appropriate wires of the USB cable

## Sketch

SevSeg, Wire, DS3231 libraries must be installed for the modules to work properly.

First of all, you need to configure the real-time module. After assembling the circuit, you need to fill in the sketch [Setting time](https://github.com/kzavadskiy/ValentineBox/blob/master/Setting%20time) on Arduino nano with installed battery in module DS3231. 

After that, you can fill the main [sketch] (https://github.com/kzavadskiy/ValentineBox/blob/master/box_sketch) with disconnected contacts SCA, SCL.

The variable dateWeGotTogether must record your memorable date in unixtime format. To do this, use the date converter https://www.unixtimestamp.com/index.php

After checking the operation, you can assemble the box, when the power is off, the real-time module saves the date and time, and after connecting to the power supply via USB cable, the date remains relevant.

  



