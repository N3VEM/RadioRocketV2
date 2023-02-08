# Radio Rocket Version 2 - Code Name Odori
Repository for version 2 of the radio rocket!
I'm just starting to capture details here.  Plan is to have this mostly fleshed out ahead of the Ham Radio QSO Today Expo in March, where I will be doing a presentation on this project.

This repository contains information related to version 2 of my [radio rocket project.](https://n3vem.com/rocket)

## APRS in the Rocket
APRS tracking is used in the rocket primarily for position data, mapping, and tracking. A 'fun' challenge here will be to see how far away the rocket gets picked directly via an RF APRS station or I-gate.

#### Bill of Materials for APRS in the Rocket
* [lightAPRS-W 2.0](https://www.qrp-labs.com/lightaprsw2.html).
  * Set up according to the information available on the [lightAPRS-W 2.0 github page.](https://github.com/lightaprs/LightAPRS-W-2.0), with modifications.

## LoRa & Telemetry in the Rocket
The rocket uses 70cm LoRa to send telemetry packets, relay messages, and respond to commands.

#### Bill of Materials for LoRa and Telemetry in the Rocket
* PJRC Teensy
* Adafruit LoRa Breakout
* (2) Relay boards
* sensor breakout 1
* sensor breakout 2
* sensor breakout 3
* sensor breakout 4

## Ground Station
The ground station is a single board computer, LoRa feather module, SDRplay Dongle, and all the associated wiring and power components, built into a project enclosure. It's primary purpose is to receive the LoRa and APRS data, and then act as a server to serve up that data via node-red and/or sound packet modem to a web browser and APRS client running on a connected device (a laptop, tablet, etc.)

#### Bill of Materials for the Ground Station
* LePotato
* Adafruit LoRa Feather
* SDRplay Dongle
* power stuff
* enclosure

## Node-Red - Served by the Ground Station
a node red dashboard served up by the ground station can display the telemetry data sent by the rocket.  

