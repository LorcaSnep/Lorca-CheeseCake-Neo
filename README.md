# Lorca-CheeseCake-Neo
## Overview:
To begin, this repository serves as an archive of my work relating to this project for the purposes of my university studies. All items in this repository are work in progress and are NOT finalized

Having used a set of Cheesecake Blueberry trackers (Design by Sorakage) for some time, I quite like them.  The hardware is well designed and the compact design of all the components makes everything extremely comfortable for long-term wear.

However, the ESP-12F processor is the one pain point that I have had with these trackers.  Of the set of 6 modules I purchased and installed on a set of 6 boards, half of them had connectivity issues.  Also, they are quite expensive to get from Digikey at almost 7 USD per piece.  As the ESP8266 has been discontinued by Espressif, there is a limit for how long the ESP12F will be available.  I began this project with two goals; design a new board based on the ESP32-C3, utilize parts only from Mouser and Digikey to limit the impact of tarrifs, and keep the form factor the same so the boards can be swapped into existing cases.  I have borrowed sections of the schematics from my other "Lorca-Throttle" project.  These boards use the ESP32-C3-MINI micro processor, CP2102 USB to UART transceiver, BQ24075RGTR battery management chip, LM3671MF Buck converter, and ICM-45686 IMU.  Two additional versions of this design are included.  One with a 5 pin AUX connector for a secondary IMU, and one designed for the LSM6DSVTR IMU. 

I also designed two PCBs for AUX IMUs.  One for the ICM-45686 and one for the LSM6DSVTR.  These are simple boards with just the IMU, the necessary passives, and the 5 pin AUX connector.

I have nicknamed these designs of trackers Pineapple as all of the other variants of the Cheesecake trackers have a food nickname.

Schematics and Bill of Materials are included in the folder for each variant of the "Pineapple" trackers.  Additionally, a document is in the folder for each variant that details the required firmware settings in the SlimeVR Firmware Flasher for these trackers.  These settings are as they exist as of 6/16/26 and may change in the future as SlimeVR continues to adapt.

## Status:
As of 7/28/26 I have built and tested a set of 6 ICM-45686 trackers, and 2 ICM-45686 + AUX trackers.  They are all working extremely well and they fit very nicely in the Cheesecake hardware.  The secondary IMU assemblies have worked out very nicely.  There are a couple of quirks with this design.  First and foremost, for some reason these boards will not work with the firmware flasher built into SlimeVR.  I cannot figure out the cause of this but I have narrowed it down to just the installer and not the firmware.  The firmware successfully installs by using the old Butterscotch web flasher and it can be successfully installed by manually compiling it with VScode.

At this point I would consider the design of the PCBs finalized.  There are two remaining tasks that need to be completed before I consider this project completed.  I would like to upload every required 3D print file to this project so every required component is in one location.  Additionally, I would like to design a version of the charging dock pcb with the same goal as the Pineapple tracker.  To swap the components to ones easily obtained from Mouser or Digikey.

## Pineapple ICM:
<p align="center">
  <img src="https://github.com/LorcaSnep/Lorca-CheeseCake-Neo/blob/1a77dbad9cac7a7ded28ecf1e120e503ebd8ce01/Images/Cheesecake%20Neo%20Pineapple%20ICM.PNG" alt="Pineapple ICM" width="400"/>
</p>

## Pineapple LSM:
<p align="center">
  <img src="https://github.com/LorcaSnep/Lorca-CheeseCake-Neo/blob/1a77dbad9cac7a7ded28ecf1e120e503ebd8ce01/Images/Cheesecake%20Neo%20Pineapple%20LSM.PNG" alt="Pineapple LSM" width="400"/>
</p>

## Pineapple ICM AUX:
<p align="center">
  <img src="https://github.com/LorcaSnep/Lorca-CheeseCake-Neo/blob/1a77dbad9cac7a7ded28ecf1e120e503ebd8ce01/Images/Cheesecake%20Neo%20Pineapple%20ICM%20AUX.PNG" alt="Pineapple ICM AUX" width="400"/>
</p>

## Pineapple ICM AUX Module:
<p align="center">
  <img src="https://github.com/LorcaSnep/Lorca-CheeseCake-Neo/blob/1a77dbad9cac7a7ded28ecf1e120e503ebd8ce01/Images/Cheesecake%20Neo%20Pineapple%20ICM%20AUX%20Module.PNG" alt="Pineapple ICM AUX Module" width="300"/>
</p>

## Pineapple LSM AUX Module:
<p align="center">
  <img src="https://github.com/LorcaSnep/Lorca-CheeseCake-Neo/blob/1a77dbad9cac7a7ded28ecf1e120e503ebd8ce01/Images/Cheesecake%20Neo%20Pineapple%20LSM%20AUX%20Module.PNG" alt="Pineapple LSM AUX Module" width="300"/>
</p>

## Ordering Information:
I have utilized JLCPCB for the production of the boards that I have tested.  The following directions are written with JLC in mind.  After downloading the zip file for the specific board variant, directly upload this to JLC.  It will automatically determine the board size and layer count.  Select the number of PCBs you want.  JLC offers quantities in multiples of 5 so plan accordingly.  Make sure to set the PCB Thickness to 1.0mm instead of the default 1.6mm.  All other options can remain as they are.  Make sure to add a solder stencil.  At the moment I have not added any pick and place files to this project and I have not compared the parts used in this projects to those that JLC keeps in stock (via LCSC).  A solder stencil will be required to assemble these boards and I recommend using a hot plate to solder these boards.

The Bill of Materials for each variant of these boards have been formatted so they can be directly uploaded to Mouser or Digikey to generate a list on each website to order components.
