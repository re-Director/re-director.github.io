---
weight: 5
title: Reverse Proxy
---

# Docker Compose behind a Reverse Proxy

You might have quite a few applications running behind a reverse proxy. The configuration should then look like this.


## Traefik

```yaml
services:
  traefik:
    image: traefik:v3.6
    restart: unless-stopped
    environment:
      SERVER_FORWARD_HEADERS_STRATEGY: native
    command:
      - "--providers.docker"
      - "--entrypoints.web.address=:80"
    ports:
      - "80:80"
    volumes:
      - /var/run/docker.sock:/var/run/docker.sock

  re-director:
    image: jensknipper/re-director:0.0.11
    restart: unless-stopped
    environment:
      SERVER_FORWARD_HEADERS_STRATEGY: native
    expose:
      - 80
    volumes:
      - re-director-data:/data
    labels:
      - "traefik.http.routers.re-director.rule=Host(`re-director.localhost`) || HostRegexp(`.+`)"
      - "traefik.http.routers.re-director.entrypoints=web"
      - "traefik.http.routers.re-director.priority=1"

volumes:
  re-director-data:
```
