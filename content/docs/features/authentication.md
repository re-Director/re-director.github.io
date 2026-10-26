---
weight: 5
title: Authentication
---

# Authentication

Currently authentication is not fully mature. It is advised to not use it for public faced instances.  
Because of that, it is for now disabled by default, but might be enabled in a future version.

It can be enabled manually using an environment variable: `RE_DIRECTOR_AUTH_ENABLED=true`

## Initial User Setup

With authentication enabled you are prompted to create a user and a password at the first login. Afterwards you are redirected to the login.

{{< image src="/screenshots/initial-user-setup-0.0.11.png" alt="user setup" loading="lazy" >}}

## Login

The login is a simple username and password login. Simply enter the credentials created during the setup.

{{< image src="/screenshots/user-login-0.0.11.png" alt="login" loading="lazy" >}}

## Example Configuration

You can check out an example configuration [here](https://github.com/re-Director/re-director/blob/master/docker/docker-compose-full.yml)