---
title: Sounder
parent: Installation
---

# Sounder

The sounder agent needs to run on a Raspberry Pi, or any computer with a sound card.

## Software

### Install (Docker)

The Docker Agent is the preferred way to run the sounder agent.

Assuming a fresh install of Rasbian Lite on a Raspberry Pi:

 1. Create a sounder in the controller, not down the controller address and sounder key
 2. Run the installer from the repo. `curl https://raw.githubusercontent.com/Open-School-Bell/sounder/refs/heads/main/install-docker.sh | sh` and enter the controller address and sounder key.

### Install (Direct Agent)

The direct agent is the same agent as the docker agent just running "bare metal", it is possibly less reliable than the Docker agent.

Assuming a fresh install of Rasbian Lite on a Raspberry Pi:

 1. Run install.sh from the repo.
    `curl https://raw.githubusercontent.com/Open-School-Bell/sounder/refs/heads/main/install.sh | sh`
 2. Create a sounder in the controller.
 3. Run the sounders enroll command on the sounder.
 4. Reboot the Pi.

#### Convert a direct agent sounder to docker.

 1. Stop the sounder service `sudo sounder stop`
 2. Disable the service `sudo update-rc.d sounder disable`.
 3. Reset the Sounder Key iin the controller.
 4. Follow the Install (Docker) instructions.

## Hardware

Suggested Hardware:

|Part|About|Link|
|:---|:----|:---|
|Raspberry Pi 5|Lowest spec is appropriate for the agent.|[https://thepihut.com/products/raspberry-pi-5](https://thepihut.com/products/raspberry-pi-5)|
|Raspberry Pi DAC+|The Pi 5 doesn't have a headphone out, but even with a Pi4 it would be ideal to use a DAC Hat to get better audio quality.|[https://thepihut.com/products/iqaudio-dac](https://thepihut.com/products/iqaudio-dac)|
|Raspberry Pi PSU|Always use a proper USB power supply for your Pi.|[https://thepihut.com/products/raspberry-pi-27w-usb-c-power-supply](https://thepihut.com/products/raspberry-pi-27w-usb-c-power-supply)|
|32GB SD Card|The agent stores nothing on the SD card, so 32GB is plenty.|[https://thepihut.com/products/noobs-preinstalled-sd-card](https://thepihut.com/products/noobs-preinstalled-sd-card)|


