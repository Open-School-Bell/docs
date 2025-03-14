---
title: Home
layout: home
nav_order: 1
---

# Open School Bell
{: .fs-9 }

{: .warning }
Open School Bell is still under development and has not been tested with widespread use.

Open School Bell is an open-source solution a modern school bell system. It not only provides a way to schedule bells but also to broadcast to the sounders, enabling effective mass-communication within your school.

![Overview]({{site.baseurl}}/assets/overview.png)

## What you'll be getting

 - Network based bell scheduling.
 - Any audio file as a bell.
 - On-demand triggering of audio files.
   - Ideal as a Lockdown alarm within school.
   - Quick distrobution allows for use as a tannoy system.
 - Active monitoring of the sounders.

## What you'll need

 - A server (could be one of your sounders) to run the docker container for the controller.
 - A Raspberry Pi to run the agent, per area of school.
 - An amplifier you can plug your Pi into.
 - A speaker wherever you want a bell wired back to the amplifier.

### You could also

 - Connect a relay to the GPIO Pins on a Raspberry Pi to an existing ringer wire so Open School Bell can run your existing bells alongside RPi sounders.
 - Connect a touch screen to one of your sounder Pis and use it as a _Lockdown Screen_

## How you'll set it up

 - Run the controller through docker, either on a server or on one of the sounder Pis.
 - Run the sounder agent on a Pi.
 - Connect the Pi to an amplifier.
 - Mount speakers on the walls, or in the ceiling of the area you want to cover.
 - Run a speaker cable from the amplifier through all the speakers in the area.
 - Configure your bell schedule on the controller.
 - Done!
