# set-network-feed - Flat List with parsing settings

**Collection:** Web API (version 2.1) > 23 Network Feed
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-network-feed`

## Description

Setting Flat List with parsing settings

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "network_feed",
  "feed-url": "https://www.feedsresource.com/new_resource",
  "username": "new_username",
  "password": "new_password",
  "feed-format": "Flat List",
  "feed-type": "IP Address",
  "update-interval": 60,
  "data-column": 1,
  "use-gateway-proxy": false,
  "fields-delimiter": ",",
  "ignore-lines-that-start-with": "!",
  "custom-header": [
    {
      "header-name": "new_header",
      "header-value": "new_value"
    }
  ]
}
```

## Example Responses

### Example 1: set-network-feed - Flat List with parsing settings
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "13bc8fb9-4fd6-42d7-8989-efd7a576c5f1",
  "name": "network_feed",
  "type": "network-feed",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1627311845840,
      "iso-8601": "2021-07-26T18:04+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1627300653362,
      "iso-8601": "2021-07-26T14:57+0300"
    },
    "creator": "WEB_API"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/NetworkFeed",
  "feed-url": "https://www.feedsresource.com/new_resource",
  "username": "new_username",
  "fields-delimiter": ",",
  "use-gateway-proxy": false,
  "certificate-id": "",
  "update-interval": 60,
  "feed-format": "Flat List",
  "feed-type": "IP Address",
  "data-column": 1,
  "custom-headers": [
    {
      "headerName": "new_header",
      "headerValue": "new_value"
    }
  ],
  "ignore-lines-that-start-with": "!"
}
```
