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