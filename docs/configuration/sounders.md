---
title: Sounders
parent: Configuration
---
# Sounders

Sounders are the configuration of the [agent]({{site.baseurl}}/docs/installation/sounder/). Agents pull the configuration from the controller after their initial enrollment, at startup, every hour, and when a call is made to `/update` on the agent.

|Option|Explination|
|:-----|:----------|
|Name|A descriptive name of the sounder.|
|IP|The IP Adress of the sounder. Used to send broadcasts and trigger config updates.|
|Ringer PIN|Defaults to 0, which disbales the feature. If set this is the GPIO pin used to control the ringer wire.|
|Screen|Defaults to off, enables the status/action screen on the sounder.|
