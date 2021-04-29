# Xiaomi Fan Lovelace Card
[![hacs_badge](https://img.shields.io/badge/HACS-Default-orange.svg)](https://github.com/custom-components/hacs)

Xiaomi Smartmi Fan Lovelace card for HASS/Home Assistant.

## Features
- Supports [HACS](https://github.com/custom-components/hacs) installation
- CSS fan blade and oscillation animation

### Toggles
- Oscillation
- Natural mode
- Child lock

### Cycling
- Speed level
- Oscillation angle
- Timer duration

## Requirements
Either of these two integrations can be used:
- [Xiaomi Mi Smart Pedestal Fan Integration](https://github.com/syssi/xiaomi_fan) v0.3.3
- [Xiaomi Mi Air Purifier & Xiaomi Mi Air Humidifier Integration](https://github.com/syssi/xiaomi_airpurifier) v0.6.9

## HACS Installation
Search for `Xiaomi Smartmi Fan Card`

## Manual Installation
1. Download `fan-xiaomi.js`
1. Copy to `www/community/lovelace-fan-xiaomi/fan-xiaomi.js`
1. Add the following to your Lovelace resources
    ``` yaml
    resources:
    - url: /community_plugin/lovelace-fan-xiaomi/fan-xiaomi.js
      type: js
    ```

## Card Configuration

Add the following to your Lovelace config `views.cards` key
```yaml
entity: fan.entity_id
name: Fan Name
type: 'custom:fan-xiaomi'
platform: xiaomi_miio_airpurifier
```
1. Replace `fan.entity_id` with your fan's entity_id and `Fan Name` with any name you'd like to name your fan with.
2. Set `platform` to either `xiaomi_miio_airpurifier` or `xiaomi_miio_fan`(if parameter not specified - `xiaomi_miio_fan` is used). For [Xiaomi Mi Air Purifier & Xiaomi Mi Air Humidifier Integration](https://github.com/syssi/xiaomi_airpurifier) you must specify `xiaomi_miio_airpurifier`, if [Xiaomi Mi Smart Pedestal Fan Integration](https://github.com/syssi/xiaomi_fan) is used then can specify `xiaomi_miio_fan` or can ommit it.

## Preview
![](preview.gif)

## Credits
[fineemb](https://github.com/fineemb) (Original author)

[shaonianzhentan](https://github.com/shaonianzhentan/)

[花神](https://github.com/yaming116)
