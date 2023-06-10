---
title: "Xiaomi ZNCJMB14LM control via MQTT"
description: "Integrate your Xiaomi ZNCJMB14LM via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2021-05-11T20:10:12Z
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# Xiaomi ZNCJMB14LM

|     |     |
|-----|-----|
| Model | ZNCJMB14LM  |
| Vendor  | [Xiaomi](/supported-devices/#v=Xiaomi)  |
| Description | Aqara S1 smart touch panel |
| Exposes | switch (state), standby_enabled, theme, beep_volume, lcd_brightness, language, screen_saver_style, standby_time, font_size, lcd_auto_brightness_enabled, homepage, screen_saver_enabled, standby_lcd_brightness, available_switches, switch_1_text_icon, switch_2_text_icon, switch_3_text_icon, linkquality |
| Picture | ![Xiaomi ZNCJMB14LM](https://www.zigbee2mqtt.io/images/devices/ZNCJMB14LM.jpg) |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->
## Notes


### Pairing
On initial boot, the device will display a message "Waiting for accessing the network" permit join and the device will be added.

If the device is already part of a network, swipe down from the top of the screen to access the Settings panel (password may be required), navigate to "Advanced", navigate to "Access New Gateway" and confirm with "Ok".
Once confirmed, proceed as per initial boot.
<!-- Notes END: Do not edit below this line -->


## OTA updates
This device supports OTA updates, for more information see [OTA updates](../guide/usage/ota_updates.md).


## Options
*[How to use device type specific configuration](../guide/configuration/devices-groups.md#specific-device-options)*

* `state_action`: State actions will also be published as 'action' when true (default false). The value must be `true` or `false`


## Exposes

### Switch (left endpoint)
The current state of this switch is in the published state under the `state_left` property (value is `ON` or `OFF`).
To control this switch publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"state_left": "ON"}`, `{"state_left": "OFF"}` or `{"state_left": "TOGGLE"}`.
To read the current state of this switch publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"state_left": ""}`.

### Switch (center endpoint)
The current state of this switch is in the published state under the `state_center` property (value is `ON` or `OFF`).
To control this switch publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"state_center": "ON"}`, `{"state_center": "OFF"}` or `{"state_center": "TOGGLE"}`.
To read the current state of this switch publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"state_center": ""}`.

### Switch (right endpoint)
The current state of this switch is in the published state under the `state_right` property (value is `ON` or `OFF`).
To control this switch publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"state_right": "ON"}`, `{"state_right": "OFF"}` or `{"state_right": "TOGGLE"}`.
To read the current state of this switch publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"state_right": ""}`.

### Standby_enabled (binary)
Enable standby.
Value can be found in the published state on the `standby_enabled` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"standby_enabled": NEW_VALUE}`.
If value equals `true` standby_enabled is ON, if `false` OFF.

### Theme (enum)
Display theme.
Value can be found in the published state on the `theme` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"theme": NEW_VALUE}`.
The possible values are: `classic`, `concise`.

### Beep_volume (enum)
Beep volume.
Value can be found in the published state on the `beep_volume` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"beep_volume": NEW_VALUE}`.
The possible values are: `mute`, `low`, `medium`, `high`.

### Lcd_brightness (numeric)
LCD brightness (will not persist if auto-brightness is enabled).
Value can be found in the published state on the `lcd_brightness` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"lcd_brightness": NEW_VALUE}`.
The minimal value is `1` and the maximum value is `100`.
The unit of this value is `%`.

### Language (enum)
Interface language.
Value can be found in the published state on the `language` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"language": NEW_VALUE}`.
The possible values are: `chinese`, `english`.

### Screen_saver_style (enum)
Screen saver style.
Value can be found in the published state on the `screen_saver_style` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"screen_saver_style": NEW_VALUE}`.
The possible values are: `classic`, `analog clock`.

### Standby_time (numeric)
Display standby time.
Value can be found in the published state on the `standby_time` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"standby_time": NEW_VALUE}`.
The minimal value is `0` and the maximum value is `65534`.
The unit of this value is `s`.

### Font_size (enum)
Display font size.
Value can be found in the published state on the `font_size` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"font_size": NEW_VALUE}`.
The possible values are: `small`, `medium`, `large`.

### Lcd_auto_brightness_enabled (binary)
Enable LCD auto brightness.
Value can be found in the published state on the `lcd_auto_brightness_enabled` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"lcd_auto_brightness_enabled": NEW_VALUE}`.
If value equals `true` lcd_auto_brightness_enabled is ON, if `false` OFF.

### Homepage (enum)
Default display homepage.
Value can be found in the published state on the `homepage` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"homepage": NEW_VALUE}`.
The possible values are: `scene`, `feel`, `thermostat`, `switch`.

### Screen_saver_enabled (binary)
Enable screen saver.
Value can be found in the published state on the `screen_saver_enabled` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"screen_saver_enabled": NEW_VALUE}`.
If value equals `true` screen_saver_enabled is ON, if `false` OFF.

### Standby_lcd_brightness (numeric)
Standby LCD brightness.
Value can be found in the published state on the `standby_lcd_brightness` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"standby_lcd_brightness": NEW_VALUE}`.
The minimal value is `1` and the maximum value is `100`.
The unit of this value is `%`.

### Available_switches (enum)
Control which switches are available in the switches screen (none disables switches screen).
Value can be found in the published state on the `available_switches` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"available_switches": NEW_VALUE}`.
The possible values are: `none`, `1`, `2`, `3`, `1 and 2`, `1 and 3`, `2 and 3`, `all`.

### Switch_1_text_icon (composite)
Switch 1 text and icon.
Can be set by publishing to `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"switch_1_text_icon": {"switch_1_icon": VALUE, "switch_1_text": VALUE}}`
- `switch_1_icon` (enum): Icon allowed values: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`, `10`, `11`
- `switch_1_text` (text): Text 

### Switch_2_text_icon (composite)
Switch 2 text and icon.
Can be set by publishing to `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"switch_2_text_icon": {"switch_2_icon": VALUE, "switch_2_text": VALUE}}`
- `switch_2_icon` (enum): Icon allowed values: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`, `10`, `11`
- `switch_2_text` (text): Text 

### Switch_3_text_icon (composite)
Switch 3 text and icon.
Can be set by publishing to `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"switch_3_text_icon": {"switch_3_icon": VALUE, "switch_3_text": VALUE}}`
- `switch_3_icon` (enum): Icon allowed values: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`, `10`, `11`
- `switch_3_text` (text): Text 

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.

