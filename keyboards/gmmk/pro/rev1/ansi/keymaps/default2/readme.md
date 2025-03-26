# Custom QMK Firmware for GMMK Pro

## Background

This is my personal QMK setup modified and based on https://github.com/2Manchu/gmmk-pro-qmk. With improvments, regarding saving the state of the rgb lighting (QMK_FANCY_ALL, QMK_FANCY_SIDE,USER_SOLID_SIDE) to EEPROM and layer updates.

## Usage and Controls

| Type                | Description |
| -----------         | ----------- |
| QMK_FANCY_ALL       | QMK built-in RGB effects (rainbow, reactive, etc) displayed on all keys and side LEDs |
| QMK_FANCY_SIDE      | QMK built-in RGB effects (rainbow, reactive, etc) displayed on only the side LEDs     |
| USER_SOLID_SIDE     | User-defined solid color displayed on only the side LEDs                              |

### For `QMK_FANCY_*` lighting types:

| Key Combo                   | Lighting action taken                                                           |
| -----------                 | -----------                                                                     |
| Left Shift                  | Scroll through QMK RGB lighting effects (rainbow, reactive, etc)                |
| Left Control                | Increase/decrease hue (color) value for selected effect                         |
| Left Alt                    | Increase/decrease saturation value for selected effect                          |
| Left Control + Alt          | Increase/decrease brightness value for selected effect                          |
| Right Shift                 | Increase/decrease speed for moving/reactive RGB, gradient width for static RGB  |
| Left Shift + Encoder Press  | Toggle all lighting on/off (persists after power loss)                          |
| Right Ctrl + Encoder Press  | Save selected effect, HSB, and speed to EEPROM (persists after power loss)      |

### For `USER_SOLID_SIDE` lighting type:

| Key Combo                   | Lighting action taken                                                           |
| -----------                 | -----------                                                                     |
| Left Control                | Increase/decrease hue (color) value for selected effect                         |
| Left Alt                    | Increase/decrease saturation value for selected effect                          |
| Left Control + Alt          | Increase/decrease brightness value for selected effect                          |
| Left Shift + Encoder Press  | Toggle all lighting on/off (persists after power loss)                          |
| Right Ctrl + Encoder Press  | Save selected effect, HSB, and speed to EEPROM (persists after power loss)   

### To access the 3 types of lighting:

| Key Combo                   | Lighting type selected                                                                    |
| -----------                 | -----------                                                                               |
| Left Ctrl + Encoder Press   | Toggle between `USER_SOLID_SIDE` and `QMK_FANCY_ALL`. Initial press defaults to user      |
| Left Alt + Encoder Press    | Toggle between `QMK_FANCY_SIDE` and `QMK_FANCY_ALL`. Initial press defaults to fancy side |