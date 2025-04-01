---
title: Ringer Wire
parent: Installation
---
# Ringer Wire

Open School Bell can use the GPIO pins on a Raspberry Pi connected to a relay to operate _ringer wire_ bell systems. This essentially means that if you have a switch to ring your bells OSB can connect into that and ring the bells for you.

> You can find the GPIO Pin Number for the controller using `cat /sys/kernel/debug/gpio`. If using GPIO17 on a Pi5 the pin number is 588, `gpio-588 (GPIO17              )`