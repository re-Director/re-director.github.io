---
weight: 2
title: Manage Redirects
---

# Manage Redirects

The UI to manage your redirects is shown in the following screenshot:
{{< image src="/screenshots/manage-redirects-0.0.11.png" alt="manage redirects UI" loading="lazy" >}}

Filter redirects in the filter bar in the top left
each redirect has actions on the right to edit, activate/deactivate and delete the redirect
you can change the pagination on the bottom of the list

## Creating a Redirect

You can create redirects using the button on the top right corner. After clicking the button, a popup simirlar to the following screenshot appears:

{{< image src="/screenshots/create-redirect-0.0.11.png" alt="create redirects UI" loading="lazy" >}}

You can set the following parameters:
- `Source`: The URL to redirect: the URL you type.
- `Target`: The URL to redirect to: the URL you want to go.
- `Status Code`: You can choose between the following HTTP Status Codes:
    - `301 - Moved Permanently`: The resource is temporarily available at a different URL
    - `302 - Found`: The resource has permanently moved to a new URL.
    - `307 - Temporary Redirect`: The resource is temporarily available at a different URL. The client must preserve the original HTTP method and request body when following the redirect.
    - `308 - Permanent Redirect`: The resource has permanently moved to a new URL. The client must preserve the original HTTP method and request body when following the redirect.
- `Path Forwarding`: Preserves the original request path (e.g., `/page/2`) when redirecting to the target URL.
- `Query Forwarding`: Preserves the original query string (e.g., `?page=2&sort=asc`) when redirecting to the target URL.