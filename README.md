# Zooz Z-Wave Device Blueprints for HomeAssistant

This repository contains a collection of blueprint automations to control and configure
several [Zooz Z-Wave](https://www.getzooz.com/products/) products. Among other features,
it's possible to easily set actions for all input actions (press 1x, 2x, 3x, 4x and 5x, hold and release).

Important configuration settings are automatically set on the devices to prepare them for use,
and some settings -- such as LED color and local physical control -- are easily configurable.

The automations automatically set configuration settings:

* Enabling scene control
* Disabling paddle programming mode (firmware-dependent)
* Disables LED flashing on parameter changes (firmware-dependent)

## Supported Devices and Automations

### Dimmers/Switches (ZEN76 and ZEN77)

* Key press events (1x, 2x, 3x, 4x, 5x, hold and release) for both on/bright and off/dim
* Supports: 
  * [ZEN76 S2 On/Off Switch](https://www.getzooz.com/zooz-zen76-s2-700-series-switch/)
  * [ZEN77 S2 Dimmer](https://www.getzooz.com/zooz-zen77-s2-dimmer/)

### Scene Controller (ZEN32)

Full control of [ZEN32 scene controller](https://www.getzooz.com/zooz-zen32-scene-controller/)

* Key press events (1x, 2x, 3x, 4x and 5x, hold and release) for all 5 buttons
* Configure built-in relay: Disable local control or re-assign to one of the smaller scene buttons
* Status indicators: Set status for each LED based on any other entity

#### ZEN32 Cover Control

Control up to 5 [cover](https://www.home-assistant.io/integrations/cover/) devices such as garage doors or roller shades.

* LED indicator shows the state of covers: one color (customizable) if any are open, another if all are closed.
* Press button 1x to activate **Cover 1**, 2x to activate **Cover 2**, etc
* Hold to close all covers

#### ZEN32 Custom Scene

Set up to 9 lights each to a specific brightness, assigned to a specific scene control button.

* LED indicator shows the state of the scene based on real device state -- even if it was manually configured
* Press button once to activate the scene. If the scene is already active, it is turned off
* Press button twice to turn on all lights to 100%
* Hold button to turn off all lights

### Relays (ZEN51 and ZEN52)

* Key press events (1x, 2x, 3x, 4x and 5x, hold and release) for input(s)
* Configure built-in relay: Disable local control or re-assign to one of the smaller scene buttons
* Supports:
  * [ZEN51 Dry Contact Relay](https://www.getzooz.com/zooz-zen51-dry-contact-relay/)
  * [ZEN52 Double Relay](https://www.getzooz.com/zooz-zen52-double-relay/)
