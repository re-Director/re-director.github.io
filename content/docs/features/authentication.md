---
weight: 5
title: Authentication
---

# Authentication

Currently authentication is not fully mature. It is advised to not use it for public faced instances.  
Because of that it is for now disabled by default, but might be enabled in a future version.

It can be enabled using an environment variable: `RE_DIRECTOR_AUTH_ENABLED=true`

## Initial User Setup

With authentication enabled you are prompted to create a user and a password at the first login. Afterwards you are redirected to the login.

{{< image src="/screenshots/initial-user-setup-0.0.11.png" alt="" title="" loading="lazy" >}}

## Login

The login is a simple username and password login. Simply enter the credentials created during the setup.

{{< image src="/screenshots/user-login-0.0.11.png" alt="" title="" loading="lazy" >}}
