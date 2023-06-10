---
title: "TuYa TS0601_thermostat_3 control via MQTT"
description: "Integrate your TuYa TS0601_thermostat_3 via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2023-01-01T08:59:10
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# TuYa TS0601_thermostat_3

|     |     |
|-----|-----|
| Model | TS0601_thermostat_3  |
| Vendor  | [TuYa](/supported-devices/#v=TuYa)  |
| Description | Thermostatic radiator valve |
| Exposes | lock (state), battery_low, climate (current_heating_setpoint, local_temperature, system_mode, running_state, local_temperature_calibration), scale_protection, frost_protection, error, linkquality |
| Picture | ![TuYa TS0601_thermostat_3](https://www.zigbee2mqtt.io/images/devices/TS0601_thermostat_3.jpg) |
| White-label | Avatto ME167 |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->
## Notes
### Pairing
You can pair this device by setting device to manual mode by short press rotary button (until clock symbol is not displayed), setting temperature to "OF" by rotating left, then press and hold rotary button. Network symbol will start to blink.
<!-- Notes END: Do not edit below this line -->




## Exposes

### Lock 
The current state of this lock is in the published state under the `child_lock` property (value is `LOCK` or `UNLOCK`).
To control this lock publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"child_lock": "LOCK"}` or `{"child_lock": "UNLOCK"}`.
It's not possible to read (`/get`) this value.

### Battery_low (binary)
Indicates if the battery of this device is almost empty.
Value can be found in the published state on the `battery_low` property.
It's not possible to read (`/get`) or write (`/set`) this value.
If value equals `true` battery_low is ON, if `false` OFF.

### Climate 
This climate device supports the following features: `current_heating_setpoint`, `local_temperature`, `system_mode`, `running_state`, `local_temperature_calibration`.
- `current_heating_setpoint`: Temperature setpoint. To control publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"current_heating_setpoint": VALUE}` where `VALUE` is the °C between `5` and `35`. Reading (`/get`) this attribute is not possible.
- `local_temperature`: Current temperature measured on the device (in °C). Reading (`/get`) this attribute is not possible.
- `system_mode`: Mode of this device. To control publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"system_mode": VALUE}` where `VALUE` is one of: `auto`, `heat`, `off`. Reading (`/get`) this attribute is not possible.
- `running_state`: The current running state. Possible values are: `idle`, `heat`. Reading (`/get`) this attribute is not possible.
- `local_temperature_calibration`: Offset to be used in the local_temperature. To control publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"local_temperature_calibration": VALUE}.`The minimal value is `-3` and the maximum value is `3` with a step size of `1`.

### Scale_protection (binary)
If the heat sink is not fully opened within two weeks or is not used for a long time, the valve will be blocked due to silting up and the heat sink will not be able to be used. To ensure normal use of the heat sink, the controller will automatically open the valve fully every two weeks. It will run for 30 seconds per time with the screen displaying "Ad", then return to its normal working state again..
Value can be found in the published state on the `scale_protection` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"scale_protection": NEW_VALUE}`.
If value equals `ON` scale_protection is ON, if `OFF` OFF.

### Frost_protection (binary)
When the room temperature is lower than 5 °C, the valve opens; when the temperature rises to 8 °C, the valve closes..
Value can be found in the published state on the `frost_protection` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"frost_protection": NEW_VALUE}`.
If value equals `ON` frost_protection is ON, if `OFF` OFF.

### Error (numeric)
If NTC is damaged, "Er" will be on the TRV display..
Value can be found in the published state on the `error` property.
It's not possible to read (`/get`) or write (`/set`) this value.

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.

