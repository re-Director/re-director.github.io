---
weight: 5
title: Logging
---

# Logging

re:Director provides different configuration options for logging.

## Log file

By default, a log file named `re-director.log` will be written into the volume of the container. 
Another way to get the logs is the [docker logs command](https://docs.docker.com/reference/cli/docker/container/logs/).

## Log Levels

You can raise the logging level by setting the following environment variable: `LOGGING_LEVEL_ROOT`. The following levels are allowed:
- `TRACE`
- `DEBUG`
- `INFO`
- `WARN`
- `ERROR`

Here the severity is ordered from low to high.
By choosing a higher severity, lower severity logs will not be logged, e.g. the level `ERROR` will only print error logs. The lower ones will include the higher level severities.

The default level is `WARN`.