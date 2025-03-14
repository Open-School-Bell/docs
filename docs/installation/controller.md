---
title: Controller
parent: Installation
---

# Controller

The Controller is best run through Docker. 

The Docker container is built for amd64 and arm64, meaning that for single sounder systems it is possible to run your controller on a Raspberry Pi.

## Docker Compose

There are 2 containers that need to be running for the controller. `openschoolbell/controller` which runs the Remix app, and `openschoolbell/tts` which provides a text to speech endpoint and generation with Piper.

```yml
services:
 controller:
    image: openschoolbell/controller:main
    restart: always
    command: ['osb-remix']
    environment:
      DATABASE_URL: file:./data/db.db
      TTS_API: http://tts-api:8080/piper
      JWT_KEY: your-super-secret-key
    volumes:
      - /path/to/data:/app/prisma/data
      - /path/to/sounds:/app/public/sounds
    ports:
      - 3000:3000

 tts-api:
    image: openschoolbell/tts:main
```

For volumes `/app/prisma/data` stores the SQLite database, and `/app/public/sounds` stores the uploaded audio files.