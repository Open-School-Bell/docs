---
title: Toubleshooting
nav_order: 50
layout: page
---
# Toubleshooting

## Sounder

### No audio with DAC+

The best way to test audio is to use the `mpg321` command on the sounder with one your your sounds (`/var/osb/sounder/sounds`). If this give an error about device being in use this is most likely a known bug with the DAC+Pi where after a reboot the DAC is not detected.

The best fix is to de-power the Pi for 10+ seconds then boot it up again.

We have found in testing that with a few reboots it might come to life, if access isn't easy.

### Bell times are slightly out

By default NTP is switched off on the Pi, enable it by editing `/etc/systemd/timesyncd.conf`. You can set `NTP=` to `pool.ntp.org` or even better a time-server in your school, like the primary domain controller.