---
title: "SONOFF ZBDongle-E control via MQTT"
description: "Integrate your SONOFF ZBDongle-E via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2022-09-30T20:52:51
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# SONOFF ZBDongle-E

|     |     |
|-----|-----|
| Model | ZBDongle-E  |
| Vendor  | [SONOFF](/supported-devices/#v=SONOFF)  |
| Description | Sonoff Zigbee 3.0 USB Dongle Plus (EFR32MG21) with router firmware |
| Exposes | light_indicator_level, linkquality |
| Picture | ![SONOFF ZBDongle-E](https://www.zigbee2mqtt.io/images/devices/ZBDongle-E.jpg) |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->
## Notes

### How to create a SONOFF ZBDongle-E Router
You can create a powerful Zigbee router from an ordinary Sonoff Zigbee 3.0 USB Dongle Plus (Model "ZBDongle-E" with EFR32MG21 chip) by flashing a router firmware onto the device. You can find the official guide for flashing the device here: [SONOFF Zigbee 3.0 USB dongle plus firmware flashing](https://sonoff.tech/wp-content/uploads/2022/11/SONOFF-Zigbee-3.0-USB-dongle-plus-firmware-flashing-.pdf). The guide also contains the link to the official [SONOFF Router Firmware for the ZBDongle-E](https://github.com/itead/Sonoff_Zigbee_Dongle_Firmware/tree/master/Dongle-E/Router).
### Hints
The guide from SONOFF is not very detailed. Here are some additional hints:
* First, you have to disassemble the device and pull the logic board out of its housing. You need a **J00 Phillips screwdriver** for this.
  <img src="https://www.zigbee2mqtt.io/images/guides/SONOFF-DongleE-Router/dongle-e-screws.jpg" width="130" height="129"/>
  <img src="https://www.zigbee2mqtt.io/images/guides/SONOFF-DongleE-Router/dongle-e-board-in-housing.jpg" width="130" height="117"/>
* Second, you need a **software supporting the [XMODEM file transfer protocol](https://en.wikipedia.org/wiki/XMODEM)** for sending the firmware image to the device. On Debian Linux like Ubuntu you can use lrzsz, 
  * install XMODEM transfer protocol and terminal emulator Putty with 
  
      `sudo apt install lrzsz putty`
  * user needs to be in dialout group in order to access serial ports
      
      `sudo adduser $USER dialout`
  * log in and out so that group membership comes into effect
* Third, you must operate on the naked logic board while it is plugged in. This is a lot easier if you use a **USB extension cable**.
* Forth, to enter the Bootloader Mode, you have to
  * Plug the device in
  * Connect to the device with the serial software (for serial connection parameters, see guide)
      
      `putty -serial -sercfg 115200,8,n,1 /dev/ttyACM0`  
      <img src="../../docs/images/putty-bootloader-1.png" width="350" height="250"/>

  * Press and hold the "BOOT" button (upper button in the lower right corner next to the USB plug in the photo below)
  * and then press the "RST." button (lower button in the lower right corner next to the USB plug in the photo below) to restart the device 
  <img src="https://www.zigbee2mqtt.io/images/guides/SONOFF-DongleE-Router/dongle-e-naked.jpg" width="648" height="242"/>
* Fifth, to upload the file, in the bootloader terminal press '1' to initiate the upload  
  <img src="../../docs/images/putty-bootloader-2.png" width="350" height="250"/>
  * Open another terminal on the host system to send the file through XMODEM    

      `sx Z3RouterUSBDonlge_EZNet6.10.3_V1.0.0.gbl < /dev/ttyACM0 > /dev/ttyACM0`
  * Wait for 'Serial upload complete', then press '2' in the Bootloader Terminal to restart the dongle.
* Finally, the dongle LED blinks green, inidicating it is in paring mode. Pair as usual with Z2M.
<!-- Notes END: Do not edit below this line -->




## Exposes

### Light_indicator_level (numeric)
Brightness of the indicator light.
Value can be found in the published state on the `light_indicator_level` property.
It's not possible to read (`/get`) or write (`/set`) this value.

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.

