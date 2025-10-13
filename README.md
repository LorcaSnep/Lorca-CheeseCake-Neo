# Lorca-CheeseCake-Neo
## Overview:
To begin, this repository serves as an archive of my work relating to this project for the purposes of my university studies. All items in this repository are work in progress and are NOT finalized

Having used a set of Cheesecake Blueberry trackers for some time, I quite like them.  The hardware is well designed and the compact design of all the components makes everything extremely comfortable for long-term wear.

However, the ESP-12F processor is the one pain point that I have had with these trackers.  Of the set of 6 modules I purchased and installed on a set of 6 boards, half of them had connectivity issues.  Also, they are quite expensive to get from Digikey at almost 7 USD per piece.  As the ESP8266 has been discontinued by Espressif, there is a limit for how long the ESP12F will be available.  I began this project with two goals; design a new board based on the ESP32-C3, utilize parts only from Digikey to limit the impact of tarrifs, and keep the form factor the same so the boards can be swapped into existing cases.  I have borrowed sections of the schematics from my other "Lorca-Throttle" project.  These boards use the ESP32-C3-MINI micro processor, CP2102 USB to UART transceiver, BQ24075RGTR battery management chip, LM3671MF Buck converter, and LSM6DSVTR IMU.  A second version with an AUX port is included for use with an auxilary IMU.

## Status:
