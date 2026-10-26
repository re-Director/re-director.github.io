---
weight: 6
title: Caching
---

# Caching

To keep the latency that re:Director introduces as small as possible, caching is implemented.

## Manually clear Caches

You can clear the Caches manually in the settings.

## Deactivate Caching

Set the environment variable `SPRING_CACHE_TYPE=none`

### Example Configuration

You can check out an example configuration [here](https://github.com/re-Director/re-director/blob/master/docker/docker-compose-full.yml)