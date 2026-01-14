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
    image: traefik:v3.4
    command:
      - "--providers.docker"
      - "--entrypoints.web.address=:80"
    ports:
      - "80:80"
    volumes:
      - /var/run/docker.sock:/var/run/docker.sock

  re-director:
    image: jensknipper/re-director:0.0.6
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

## Nginx

If you already use Nginx I would recommend against using re:Director and use [Nginx Proxy Manager (NPM)](https://nginxproxymanager.com/) instead.