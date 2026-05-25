# add-network-feed - JSON with parsing settings

**Collection:** Web API (version 2.1) > 23 Network Feed
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-network-feed`

## Description

Adding JSON with parsing settings

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
  "feed-format": "JSON",
  "feed-type": "IP Address",
  "update-interval": 60,
  "json-query": ".[]|.ips",
  "use-gateway-proxy": false,
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

### Example 1: add-network-feed - JSON with parsing settings
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "c66e2256-5284-49de-b70a-af6316661884",
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
      "posix": 1637654581803,
      "iso-8601": "2021-11-23T10:03+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1637654581803,
      "iso-8601": "2021-11-23T10:03+0200"
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
  "fields-delimiter": "",
  "use-gateway-proxy": false,
  "certificate-id": "",
  "update-interval": 60,
  "data-column": 1,
  "feed-format": "JSON",
  "feed-type": "IP Address",
  "json-query": ".[]|.ips",
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
  "ignore-lines-that-start-with": "#"
}
```
