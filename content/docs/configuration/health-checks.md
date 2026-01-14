---
weight: 4
title: Health Checks
---

# Health Checks

Re:Director uses [Spring Actuator](https://docs.spring.io/spring-boot/how-to/actuator.html) to do health checks.
  
The following checks are available.
- overall health: `/actuator/health`
- liveness: `/actuator/health/liveness`
- readiness: `/actuator/health/readiness`

When the application is healthy a JSON like this is returned

```json
{
  "status": "UP"
}
```

Possible results for the status attribute are:
- `UP`
- `DOWN`
- `OUT_OF_SERVICE