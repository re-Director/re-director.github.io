---
weight: 3
title: Filter Redirects
---

# Filter Redirects

Filtering redirects is the core feature of any redirect manager like re:Director. It allows you to setup redirects in the following form:
- From `re-director.internal` to `re-director.github.io` 
    - Source and Target configuration
- From `re-director.internal?status=ACTIVE` to `re-director.github.io?status=ACTIVE`
    - Source and Target configuration 
    - Query Forwarding option active
- From `re-director.internal/redirects` to `re-director.github.io/redirects` 
    - Source and Target configuration 
    - Path Forwarding option active
- From `re-director.internal/redirects?status=ACTIVE` to `re-director.github.io/redirects?status=ACTIVE`
    - Source and Target configuration 
    -  Path Forwarding option active
    -  Query Forwarding option active