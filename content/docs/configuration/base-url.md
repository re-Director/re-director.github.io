---
weight: 3
title: Base URL
---

# Base URL

You can configure a base URL for re:Director. That way a missing or disabled redirect will show a certain page that informs the user about the missing redirect.  To activate the feature you just have to set the following environment variable: `RE_DIRECTOR_BASE_URL=http://<your-domain>`

As soon as the feature is activated, you may see the following text when a missing redirect is hit:

> No redirect found!  
For the URL you specified, there is currently no active redirect configured. 

The URL changes to the following: `<base-url>/no-redirect-found`

An example can be seen on the following example page:
{{< image src="/screenshots/base-url-0.0.11.png" alt="base URL UI" loading="lazy" >}}


## Troubleshooting

In case you encounter any troubles, it is advised to check the logs.  
A successful configuration should contain the following entry: `Specified base url is: 'http://re-director.internal'`

If the specified value is not a URL, it will be ignored and you can see the following warning in the logs: `Could not parse specified base url to URI: ''`

Remember, that the log level should be [set to INFO](/docs/configuration/logging/#log-levels).

## Example Configuration

You can check out an example configuration [here](https://github.com/re-Director/re-director/blob/master/docker/docker-compose-full.yml)