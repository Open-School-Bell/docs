---
title: Sounder
parent: Installation
---

# Sounder

The sounder agent needs to run on a Raspverry Pi, or any computer with a sound card.

## Software

### Install

Assuming a fresh install of Rasbian Lite on a Raspberry Pi:

 1. Run install.sh from the repo.
    `curl https://raw.githubusercontent.com/Open-School-Bell/sounder/refs/heads/main/install.sh | sh`
 2. Create a sounder in the controller.
 3. Run the sounders enroll command on the sounder.
 4. Reboot the Pi.

## Hardware

Suggested Hardware:

|Part|About|Link|
|:---|:----|:---|
|Raspberry Pi 5|Lowest spec is appropriate for the agent.|https://thepihut.com/products/raspberry-pi-5|
|Raspberry Pi DAC+|The Pi 5 doesn't have a headphone out, but even with a Pi4 it would be ideal to use a DAC Hat to get better audio quality.|https://thepihut.com/products/iqaudio-dac|
|Raspberry Pi PSU|Always use a proper USB power supply for your Pi.|https://thepihut.com/products/raspberry-pi-27w-usb-c-power-supply|
|32GB SD Card|The agent stores nothing on the SD card, so 32GB is plenty.|https://thepihut.com/products/noobs-preinstalled-sd-card|


