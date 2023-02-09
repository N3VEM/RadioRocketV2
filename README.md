# Radio Rocket Version 2 - Code Name Odori
Repository for version 2 of the radio rocket!
I'm just starting to capture details here.  Plan is to have this mostly fleshed out ahead of the Ham Radio QSO Today Expo in March, where I will be doing a presentation on this project.

This repository contains information related to version 2 of my [radio rocket project.](https://n3vem.com/rocket)

More specific details can be round in the readme within each folder, for the various sections of the rocket.

## APRS in the Rocket
APRS tracking is used in the rocket primarily for position data, mapping, and tracking. Track how high your rocket went, and how far away it's packets were received. The APRS sled can be done stand-alone without the rest of the project, if you simply want to beacon packets, and then check aprs.fi for data. Building the APRS tracker only would rely on their being at least 1 I-Gate within range of your launch site.

## LoRa & Telemetry in the Rocket
The rocket uses 70cm LoRa to send telemetry packets, relay messages, and respond to commands.

## Ground Station
The ground station is a single board computer, LoRa feather module, SDRplay Dongle, and all the associated wiring and power components, built into a project enclosure. It's primary purpose is to receive the LoRa and APRS data, and then act as a server to serve up that data via node-red and/or sound packet modem to a web browser and APRS client running on a connected device (a laptop, tablet, etc.)

