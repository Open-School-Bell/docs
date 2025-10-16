---
title: Screen
parent: Installation
---

# Screen

The Screen element of OSB runs on a sounder.

## Software

### Install

Assuming a fresh install of Rasbian on a Raspberry Pi:

 1. Run install.sh from the repo.
    `curl https://raw.githubusercontent.com/Open-School-Bell/sounder/refs/heads/main/install.sh | sh`
 2. Create a sounder in the controller.
 3. Run the sounders enroll command on the sounder.
 4. Edit the sounder in the controller to enable the screen.
 5. Create `~/.config/autostart/osb.desktop` with the contents below.
 6. Install an emoji font `sudo apt-get install fonts-noto-color-emoji`.
 7. Reboot the Pi.

```
[Desktop Entry]
Type=Application
Exec=chromium http://localhost:3000/screen.html -kiosk
```

## Hardware

Suggested Hardware:

|Part|About|Link|
|:---|:----|:---|
|Raspberry Pi 5|Lowest spec is appropriate for the agent.|[https://thepihut.com/products/raspberry-pi-5](https://thepihut.com/products/raspberry-pi-5)|
|Raspberry Pi DAC+|The Pi 5 doesn't have a headphone out, but even with a Pi4 it would be ideal to use a DAC Hat to get better audio quality.|[https://thepihut.com/products/iqaudio-dac](https://thepihut.com/products/iqaudio-dac)|
|Raspberry Pi PSU|Always use a proper USB power supply for your Pi.|[https://thepihut.com/products/raspberry-pi-27w-usb-c-power-supply](https://thepihut.com/products/raspberry-pi-27w-usb-c-power-supply)|
|32GB SD Card|The agent stores nothing on the SD card, so 32GB is plenty.|[https://thepihut.com/products/noobs-preinstalled-sd-card](https://thepihut.com/products/noobs-preinstalled-sd-card)|
|Raspberry Pi TOuch Display 2|Touch screen to display the screen on and interact with the action buttons.|[https://thepihut.com/products/raspberry-pi-touch-display-2](https://thepihut.com/products/raspberry-pi-touch-display-2)|
|Pi Wall Bracket (3d Printed)|Housing that contains the Pi on the back of the screen and mounts flush to a wall.|[https://www.thingiverse.com/thing:7172671](https://www.thingiverse.com/thing:7172671)|