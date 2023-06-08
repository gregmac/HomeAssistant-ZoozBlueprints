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

## Basic Controls

A blueprint for each supported device that provides basic keypress events and configuration.

* [ZEN76 S2 On/Off Switch](https://www.getzooz.com/zooz-zen76-s2-700-series-switch/)
* [ZEN77 S2 Dimmer](https://www.getzooz.com/zooz-zen77-s2-dimmer/)
* [ZEN32 Scene Controller](https://www.getzooz.com/zooz-zen32-scene-controller/)
* [ZEN51 Dry Contact Relay](https://www.getzooz.com/zooz-zen51-dry-contact-relay/)
* [ZEN52 Double Relay](https://www.getzooz.com/zooz-zen52-double-relay/)

||[ZEN32<br>Scene](https://www.getzooz.com/zooz-zen32-scene-controller/)<br>[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fgregmac%2FHomeAssistant-ZoozBlueprints%2Fblob%2Fmain%2FZEN32%2520Controller.yaml)|[ZEN76<br>On/Off Switch](https://www.getzooz.com/zooz-zen76-s2-700-series-switch/)<br>[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fgregmac%2FHomeAssistant-ZoozBlueprints%2Fblob%2Fmain%2FZEN76%2520S2%2520Switch.yaml)|[ZEN77<br>Dimmer](https://www.getzooz.com/zooz-zen77-s2-dimmer/)<br>[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fgregmac%2FHomeAssistant-ZoozBlueprints%2Fblob%2Fmain%2FZEN77%2520S2%2520Dimmer.yaml)|[ZEN51<br>Relay](https://www.getzooz.com/zooz-zen51-dry-contact-relay/)<br>[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fgregmac%2FHomeAssistant-ZoozBlueprints%2Fblob%2Fmain%2FZEN51%2520Relay.yaml)|[ZEN52<br>Double Relay](https://www.getzooz.com/zooz-zen52-double-relay/)<br>[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fgregmac%2FHomeAssistant-ZoozBlueprints%2Fblob%2Fmain%2FZEN52%2520Dual%2520Relay.yaml)|
|-|:-:|:-:|:-:|:-:|:-:|
|Individual key press events (1x, 2x, 3x, 4x, 5x, hold and release)|✔|✔|✔|✔|✔|
|Update indicator state based on HA entity|✔|✖|✖|-|-|
|Choose indicator color|✔|✖|✖|-|-|
|Enable/disable local control|✔|✔|✔|✔|✔|
|Reassign local control to another button|✔|-|-|-|-|
|Enables scene control|✔|✔|✔|✔|✔|
|Disables local programming (firmware-dependent)|✔|✔|✔|-|-|


## Specialty Controls

### Zooz LED Brightness

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fgregmac%2FHomeAssistant-ZoozBlueprints%2Fblob%2Fmain%2FZooz%2520Led%2520Brightness.yaml)

Automatically set brightness of the LED indicators on Zooz devices for day and night.

* Supports: ZEN32, ZEN76, and ZEN77.

* Transitions on Sunrise or Sunset, with configurable offsets

* Running the automation manually sets the levels immediately

### ZEN32 Cover Control

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fgregmac%2FHomeAssistant-ZoozBlueprints%2Fblob%2Fmain%2FZEN32%2520Controller%2520-%2520Cover%2520Control.yaml)

Use a button on a [ZEN32 Scene Controller](https://www.getzooz.com/zooz-zen32-scene-controller/)
to control up to 5 [cover](https://www.home-assistant.io/integrations/cover/) devices such as
garage doors or roller shades.

* LED indicator shows the state of covers: one color (customizable) if any are open, another if all are closed.
* Press button 1x to activate **Cover 1**, 2x to activate **Cover 2**, etc
* Hold to close all covers

### ZEN32 Custom Scene

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fgregmac%2FHomeAssistant-ZoozBlueprints%2Fblob%2Fmain%2FZEN32%2520Controller%2520-%2520Custom%2520Scene.yaml)

Set up to 9 lights each to a specific brightness, assigned to a specific
[ZEN32 Scene Controller](https://www.getzooz.com/zooz-zen32-scene-controller/) button.

* LED indicator shows the state of the scene based on real device state -- even if it was manually configured
* Press button once to activate the scene. If the scene is already active, it is turned off
* Press button twice to turn on all lights to 100%
* Hold button to turn off all lights


