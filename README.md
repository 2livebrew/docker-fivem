# FiveM Server Container

[![Docker Pulls](https://img.shields.io/docker/pulls/2livebrew/fivem.svg)](https://hub.docker.com/r/2livebrew/fivem/)
[![Docker Stars](https://img.shields.io/docker/stars/2livebrew/fivem.svg)](https://hub.docker.com/r/2livebrew/fivem/)
[![Docker Build](https://img.shields.io/docker/automated/2livebrew/fivem.svg)](https://hub.docker.com/r/2livebrew/fivem/)
[![Docker Build Status](https://img.shields.io/docker/build/2livebrew/fivem.svg)](https://hub.docker.com/r/2livebrew/fivem/)

[FiveM](https://fivem.net/) server running on [Alpine Linux](https://hub.docker.com/_/alpine/).

## Configuration

See [example directory](https://github.com/2livebrew/docker-fivem/tree/master/example) for sample config file.

## Quickstart

```yml
fivem:
  image: 2livebrew/fivem

  volumes:
    # You must provide a server config file
    - ./server.cfg:/srv/server.cfg

    - ./resources:/srv/resources
    - ./cache:/srv/cache

  ports:
    - "30120:30120/tcp"
    - "30120:30120/udp"
```
