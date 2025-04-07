---
title: Controller
parent: Installation
---

# Controller

The Controller is best run through Docker. 

The Docker container is built for amd64 and arm64, meaning that for single sounder systems it is possible to run your controller on a Raspberry Pi.

## Docker Compose

There are 3 containers that need to be running for the controller. `openschoolbell/controller` which runs the Remix app, `openschoolbell/tts` which provides a text to speech endpoint and generation with Piper, and `redis` for the background job scheduling.

```yml
x-shared:
  osb-service: &osb-service
    environment: &osb-environment
      - DATABASE_URL=file:./data/db.db
      - TTS_API=http://tts-api:8080/piper
      - JWT_KEY=your-super-secret-key
      - REDIS_URL=osb-redis:6379
    volumes: &osb-volumes
      - /path/to/data:/app/prisma/data
      - /path/to/sounds:/app/public/sounds
    image: openschoolbell/controller:1
    restart: always
    depends_on:
      - osb-redis

services:
 osb-controller:
    <<: *osb-service
    command: ['osb-remix']
    ports:
      - 3000:3000

  osb-worker:
    <<: *osb-service
    command: ['osb-worker']
    depends_on:
      - osb-controller

 tts-api:
    image: openschoolbell/tts:1
 osb-redis:
    image: redis:7
    restart: always
    volumes:
      - ./data/redis:/data
```

For volumes `/app/prisma/data` stores the SQLite database, and `/app/public/sounds` stores the uploaded audio files.

Paste the above yaml into `docker-compose.yml` in a folder on your docker server. Typically the `data` and `sounds` folders would be in the same folder as the `docker-compose.yml`.

Once edited with the correct paths, pull down the controller and tts images with `docker compose pull`, and launch the controller with `docker compose up -d`.

## Initial Setup

Open a web browser and browse to `http://CONTROLLER_IP:3000/`. The default password is `bell`, once logged in you will be on the dashboard. 