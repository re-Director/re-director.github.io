---
weight: 5
title: FAQ
---

# FAQ

## What is re:Director?

re:Director is a free and open source redirect service. It is a selfhosted alternative to many SaaS solutions. You can use it to manage redirects to URLs, pages or sites.

## Can I redirect any domain?

Yes, you can redirect any domain, even made up TLDs.  
Just make sure to create a DNS entry pointing to re:Director and create a redirect there. Just make sure to prepend `http://` or `https://` in the address bar so the browser loads the page and does not perform a web search.

## How can I run re:Director?

You can either run it from sources or using the provided Docker container. There are examples for using it with plain Docker, Docker Compose or with Docker Compose behind a reverse proxy.

## My redirect is not working!

There might be multiple reasons. 
dns entry

# Why not use a reverse proxy?

I was self hosting my applications behind Traefik reverse proxy and defined the redirects in there. My Docker Compose file got longer and longer to the point where it was barely readable at all. Also the process of editing it was cumbersome: SSHing into the machine, editing the file with Vim and restarting the service.

I do not aim to replace a reverse proxy, but to make the redirect management easier. That way you might even want to run this app behind a reverse proxy.

In the end it's just a tool for your own comfort.Got only one or two redirects, that do not change at all - reverse proxy is probably the best way. Got a few more, that might even change regularly - this tool might save you a few steps and makes your life a little easier.

# Why not use a URL shortener?

A URL shortener usually has many more features that you do not need. Additionally they often do not provide the features you need, or only with caveats. Many of the selfhosting applications are also difficult to set up.