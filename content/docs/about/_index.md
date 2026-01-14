---
weight: 1
title: About
---

# About

re:Director lets you create redirects through a simple web interface. All you have to do is define which url should be redirected to which target. Just make sure the that the actual domain points to re:Director.
It's an open-source ([Apache License 2.0](https://github.com/re-Director/re-director/blob/master/LICENSE)) and self-hostable alternative to many SaaS solutions out there.

## Why I built this

I was self hosting my applications behind Traefik reverse proxy and defined the redirects in there. My Docker Compose file got longer and longer to the point where it was barely readable at all. Also the process of editing it was cumbersome: SSHing into the machine, editing the file with Vim and restarting the service.
I also tried out different URL shorteners, but they were either difficult to set up or where doing so many more things.

I wanted something simpler to manage my redirects, with a Web UI. I am a developer by day, so I just wrote one myself.