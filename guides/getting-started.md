---
title: Getting Started
parent: Guides
---

# Getting Started

This guide will run you through getting your controller and first sounder setup.

## Some Assumptions:

 - You have a Raspberry Pi running Raspbian Lite.
 - You have a server (or pi) with Docker and Docker Compose installed.

# Controller

 1. On your server (or docker pi) run through the [Controller Installation](/docs/installation/controller).
 1. Change your password from the _Change Password_ link on the menu.
 1. Open _Zones_ and _Add_ a zone.
 1. Open _Sounders_ and _Add_ a new sounder. Details of the options can be found in the [sounder configuration](/docs/configuration/sounders/).
 1. On your new sounder add it to your new zone.

You aren now ready to install the sounder and enroll it.

# Adding a Sounder

On the sounder Pi run through the [Sounder Installation](/docs/installation/sounder/). The enroll command can be found on the sounders page.