# add-network-feed - Flat List with parsing settings

**Collection:** Web API (version 2.0.1) > 23 Network Feed
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-network-feed`

## Description

Adding Flat List with parsing settings

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
  "feed-url": "https://www.feedsresource.com/resource",
  "username": "feed_username",
  "password": "feed_password",
  "feed-format": "Flat List",
  "feed-type": "IP Address",
  "update-interval": 60,
  "data-column": 1,
  "use-gateway-proxy": false,
  "fields-delimiter": "\t",
  "ignore-lines-that-start-with": "!",
  "custom-header": [
    {
      "header-name": "header1",
      "header-value": "value1"
    },
    {
      "header-name": "header2",
      "header-value": "value2"
    }
  ]
}
```

## Example Responses

### Example 1: add-network-feed - Flat List with parsing settings
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "2f5b7d67-6428-472f-9527-e19662574260",
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
      "posix": 1627293523483,
      "iso-8601": "2021-07-26T12:58+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1627293523483,
      "iso-8601": "2021-07-26T12:58+0300"
    },
    "creator": "WEB_API"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/NetworkFeed",
  "feed-url": "https://www.feedsresource.com/resource",
  "username": "feed_username",
  "fields-delimiter": "\t",
  "use-gateway-proxy": false,
  "certificate-id": "",
  "update-interval": 60,
  "feed-format": "Flat List",
  "feed-type": "IP Address",
  "data-column": 1,
  "custom-headers": [
    {
      "headerName": "header1",
      "headerValue": "value1"
    },
    {
      "headerName": "header2",
      "headerValue": "value2"
    }
  ],
  "ignore-lines-that-start-with": "!"
}
```
