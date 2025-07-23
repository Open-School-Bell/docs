---
title: Updating the Controller
parent: Guides
---

For the most part updating the controller is as simple as:

  1. SSH into your docker server, pi, vm, etc....
  2. cd to the folder with your `docker-compose.yml` in.
  3. Run `docker compose pull` to download the lastest images.
  4. Run `docker compose down` and `docker compose up -d` to restart the controller.

## Specific version changes

### Controller 1.2.0

Controller 1.2.0 requires TTS 2.0.0 or later. TTS 2.0.0 is a breaking change that needs your `docker-compose.yml` to be edited.

  1. Change `TTS_API=http://tts-api:8080/piper` to `TTS_API=http://tts-api`
  2. Change `image: openschoolbell/tts:1` to `image: openschoolbell/tts:2`

And then run the normal update process.