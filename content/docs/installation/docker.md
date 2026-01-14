---
weight: 4
title: Docker (Compose)
---

# Docker

An image of the application can be pulled from [Docker Hub](https://hub.docker.com/r/jensknipper/re-director).

You can run it using the following command:
```bash
docker run \
  --name re-director \
  -p 80:80 \
  -v re-director-data:/data \
  jensknipper/re-director:0.0.6
```

## Docker Compose

You can also run this application using [Docker Compose](https://docs.docker.com/compose/)
Simply save the following code into a `docker-compose.yml` file and run `docker-compose up`.

```yaml
services:
  re-director:
    image: jensknipper/re-director:0.0.6
    ports:
      - "80:80"
    volumes:
      - re-director-data:/data

volumes:
  re-director-data:
```