---
title: "TuYa ZG-102ZL control via MQTT"
description: "Integrate your TuYa ZG-102ZL via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2022-11-9T1:17:42
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# TuYa ZG-102ZL

|     |     |
|-----|-----|
| Model | ZG-102ZL  |
| Vendor  | [TuYa](/supported-devices/#v=TuYa)  |
| Description | Luminance door sensor |
| Exposes | contact, illuminance, battery, linkquality |
| Picture | ![TuYa ZG-102ZL](https://www.zigbee2mqtt.io/images/devices/ZG-102ZL.jpg) |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->
## Notes

### Pairing
To start pairing, press the button (pinhole on the side of the device) using a
pin/paperclip for approx. 5 seconds. The led will turn on, then start blinking while the
pairing process is in progress.
<!-- Notes END: Do not edit below this line -->




## Exposes

### Contact (binary)
Indicates if the contact is closed (= true) or open (= false).
Value can be found in the published state on the `contact` property.
It's not possible to read (`/get`) or write (`/set`) this value.
If value equals `false` contact is ON, if `true` OFF.

### Illuminance (numeric)
Raw measured illuminance.
Value can be found in the published state on the `illuminance` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The unit of this value is `lx`.

### Battery (numeric)
Remaining battery in %, can take up to 24 hours before reported..
Value can be found in the published state on the `battery` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `100`.
The unit of this value is `%`.

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.

