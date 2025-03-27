---
title: Connecting to a Ringer Wire
parent: Guides
---
# Connecting to a Ringer Wire

Legacy Bell systems often use a _Ringer Wire_ where a _Normally Open_ wire runs to every bell and when you _close_ the connection the bell rings. It's the simpliest way to run a bell and in a lot of cases a simple switch is in place to manually ring the bell.

If you have a bell that can be operated by closing a connection then OSB can become your bells controller through the use of the GPIO pins on the Pi and a [relay](https://thepihut.com/products/gravity-digital-10a-relay-module).

## Configuring the Sounder

Edit the sounder on the controller to set the ringer pin to the GPIO pin connected to your relay.

## Configuring the Audio

When editing an audio file there is an option for `ringerWire`. This option needs to be set to a comma seperated list of durations. `ON,OFF` e.g. `1,3` which would be on for 1 second, off for 3. It is highly reccomended that you include the off time so that if the sound is repeated a gap is left before the next on switch, although the sounder will always return the pin to _off_ after any rings.

Not every audio file needs a ringerWire, for example tannoy annoucements would be a little redundant as rings on the bell. 