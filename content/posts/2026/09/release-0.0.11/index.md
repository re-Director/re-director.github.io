---
date: 2026-09-01
tags: [release]
title: Version 0.0.11 released
type: posts
---

* add ability to secure re:Director using basic authentication
  * the feature is not 100% mature, so it is advised to not use it for public faced instances
  * for now disabled by default
  * can enabled by environment variable: `RE_DIRECTOR_AUTH_ENABLED: true`
* you can now configure a base URL for re:Director
  *  that way a missing or disabled redirects will show a certain page
  * just set the following environment variable `RE_DIRECTOR_BASE_URL: http://re-director.internal`
* only show error details to logged in users
* fixed that error pages were not shown
* fixed some possible DNS timing vulnerability in the test redirects feature
* fix some minor wordings issues and logo presentation
* prepare analytics feature - hits are now logged to the backend
* handle trailing slashes in request URLs by @steven-s-martins in https://github.com/re-Director/re-director/pull/14

**Full Changelog**: https://github.com/re-Director/re-director/compare/0.0.10...0.0.11