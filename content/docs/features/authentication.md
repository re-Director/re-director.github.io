---
weight: 5
title: Authentication
---

# Authentication

Authentication is enabled by default.  
It can be disabled manually using an environment variable: `RE_DIRECTOR_AUTH_ENABLED=false`.  
You can also set the minimum required password length: `RE_DIRECTOR_AUTH_PASSWORD_MIN_LENGTH=8`

## Initial User Setup

With authentication enabled you are prompted to create a user and a password at the first login. The minimum required passeord lenght is eight characters.  
Afterwards creating a user, you are redirected to the login.

{{< image src="/screenshots/initial-user-setup-0.0.11.png" alt="user setup" loading="lazy" >}}

## Login

The login is a simple username and password login. Simply enter the credentials created during the setup.

{{< image src="/screenshots/user-login-0.0.11.png" alt="login" loading="lazy" >}}

## Example Configuration

You can check out an example configuration [here](https://github.com/re-Director/re-director/blob/master/docker/docker-compose-full.yml)