---
title: "SONOFF SNZB-02 control via MQTT"
description: "Integrate your SONOFF SNZB-02 via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendors bridge or gateway."
addedAt: 2020-07-10T21:03:07Z
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# SONOFF SNZB-02

|     |     |
|-----|-----|
| Model | SNZB-02  |
| Vendor  | SONOFF  |
| Description | Temperature and humidity sensor |
| Exposes | battery, temperature, humidity, voltage, linkquality |
| Picture | ![SONOFF SNZB-02](https://www.zigbee2mqtt.io/images/devices/SNZB-02.jpg) |
| White-label | eWeLink RHK08 |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->
## Notes


### Pairing
Long press reset button for 5s until the LED indicator flashes three times, which means the device has entered pairing mode

### Reporting intervals
It has been reported, that the sensor reports humidity changes quite frequently (changes on 2nd digit level), but temperature changes are reported only once per hour or when temperature has changed > ~0.6°C. This results in a *staircase* development in recorded temperatures and inhibits fine-granular climate control. No resolution is known so far. See also [Homeassistant Community Forums](https://community.home-assistant.io/t/sonoff-snzb-02-temp-sensor-reporting-interval/216315/7)


### Battery
Uses a CR2450 battery
<!-- Notes END: Do not edit below this line -->


## Options
*[How to use device type specific configuration](../guide/configuration/devices-groups.md#specific-device-options)*

* `temperature_precision`: Number of digits after decimal point for temperature, takes into effect on next report of device. The value must be a number with a minimum value of `0` and with a with a maximum value of `3`

* `temperature_calibration`: Calibrates the temperature value (absolute offset), takes into effect on next report of device. The value must be a number.

* `humidity_precision`: Number of digits after decimal point for humidity, takes into effect on next report of device. The value must be a number with a minimum value of `0` and with a with a maximum value of `3`

* `humidity_calibration`: Calibrates the humidity value (absolute offset), takes into effect on next report of device. The value must be a number.


## Exposes

### Battery (numeric)
Remaining battery in %.
Value can be found in the published state on the `battery` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `100`.
The unit of this value is `%`.

### Temperature (numeric)
Measured temperature value.
Value can be found in the published state on the `temperature` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The unit of this value is `°C`.

### Humidity (numeric)
Measured relative humidity.
Value can be found in the published state on the `humidity` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The unit of this value is `%`.

### Voltage (numeric)
Voltage of the battery in millivolts.
Value can be found in the published state on the `voltage` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The unit of this value is `mV`.

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.

