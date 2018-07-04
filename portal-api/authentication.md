---
description: Authenticating your requests to securely access the MagLoft API
---

# Authentication

## User Access Token

When you logged in in the MagLoft portal, a unique code of Access Token is set for you. This Access Token is available on your Profile Information of your MagLoft Account. Keep it private and don't share it with anyone.

![This 21 character string is your personal Access Token which grants you access to all APIs.](../.gitbook/assets/access-token%20%281%29.png)

### Usage:

To use your access token, pass the it via the `X-Magloft-Accesstoken` header variable:

```
X-Magloft-Accesstoken: USER_ACCESS_TOKEN
```

{% hint style="info" %}
 If you do not include the Header request, you will get the response error "401 Unauthorised" for most API requests.
{% endhint %}

### Request Example:

```
curl -X GET -H 'X-Magloft-Accesstoken: YOUR_ACCESS_TOKEN' https://www.magloft.com/api/portal/v1/publications
```



