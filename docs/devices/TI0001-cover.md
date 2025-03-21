---
title: "Livolo TI0001-cover control via MQTT"
description: "Integrate your Livolo TI0001-cover via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendors bridge or gateway."
addedAt: 2021-03-30T20:29:35Z
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# Livolo TI0001-cover

|     |     |
|-----|-----|
| Model | TI0001-cover  |
| Vendor  | Livolo  |
| Description | Zigbee roller blind motor |
| Exposes | cover (state, position), options, moving, linkquality |
| Picture | ![Livolo TI0001-cover](https://www.zigbee2mqtt.io/images/devices/TI0001-cover.jpg) |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->
## Notes

### Pairing
Press the buttons "down" and "settings" together for 3 seconds and it blinks red and blue in pairing mode.

<!-- Notes END: Do not edit below this line -->



## Exposes

### Cover 
The current state of this cover is in the published state under the `state` property (value is `OPEN` or `CLOSE`).
To control this cover publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"state": "OPEN"}`, `{"state": "CLOSE"}`, `{"state": "STOP"}`.
It's not possible to read (`/get`) this value.
To change the position publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"position": VALUE}` where `VALUE` is a number between `0` and `100`.

### Options (composite)
Can be set by publishing to `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"options": {"motor_speed": VALUE, "motor_direction": VALUE}}`
- `motor_speed` (numeric): Motor speed. 
- `motor_direction` (enum): Motor direction. Allowed values: `FORWARD`, `REVERSE`

### Moving (binary)
Motor is moving.
Value can be found in the published state on the `moving` property.
It's not possible to read (`/get`) or write (`/set`) this value.
If value equals `undefined` moving is ON, if `undefined` OFF.

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.

