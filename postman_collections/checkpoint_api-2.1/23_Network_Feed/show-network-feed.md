# show-network-feed

**Collection:** Web API (version 2.1) > 23 Network Feed
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-network-feed`

## Description

Showing a Network Feed

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "network_feed"
}
```

## Example Responses

### Example 1: show-network-feed
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "8fa9d57c-37a0-4aa3-8d74-52d4a84a1394",
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
      "posix": 1627311263394,
      "iso-8601": "2021-07-26T17:54+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1627311263394,
      "iso-8601": "2021-07-26T17:54+0300"
    },
    "creator": "WEB_API"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/NetworkFeed",
  "feed-url": "https://www.feedsresource.com/resource",
  "username": "feed_username",
  "fields-delimiter": "\n",
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
