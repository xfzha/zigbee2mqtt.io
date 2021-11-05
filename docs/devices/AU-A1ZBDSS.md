---
title: "Aurora Lighting AU-A1ZBDSS control via MQTT"
description: "Integrate your Aurora Lighting AU-A1ZBDSS via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendors bridge or gateway."
addedAt: 2021-03-30T20:29:35Z
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# Aurora Lighting AU-A1ZBDSS

|     |     |
|-----|-----|
| Model | AU-A1ZBDSS  |
| Vendor  | Aurora Lighting  |
| Description | Double smart socket UK |
| Exposes | switch (state), power, linkquality |
| Picture | ![Aurora Lighting AU-A1ZBDSS](https://www.zigbee2mqtt.io/images/devices/AU-A1ZBDSS.jpg) |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->


<!-- Notes END: Do not edit below this line -->



## Exposes

### Switch (left endpoint)
The current state of this switch is in the published state under the `state_left` property (value is `ON` or `OFF`).
To control this switch publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"state_left": "ON"}`, `{"state_left": "OFF"}` or `{"state_left": "TOGGLE"}`.
To read the current state of this switch publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"state_left": ""}`.

### Switch (right endpoint)
The current state of this switch is in the published state under the `state_right` property (value is `ON` or `OFF`).
To control this switch publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"state_right": "ON"}`, `{"state_right": "OFF"}` or `{"state_right": "TOGGLE"}`.
To read the current state of this switch publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"state_right": ""}`.

### Power (numeric, left endpoint)
Instantaneous measured power.
Value can be found in the published state on the `power_left` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The unit of this value is `W`.

### Power (numeric, right endpoint)
Instantaneous measured power.
Value can be found in the published state on the `power_right` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The unit of this value is `W`.

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.

