# set-network-feed - JSON with parsing settings

**Collection:** Web API (version 2.1) > 23 Network Feed
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-network-feed`

## Description

Setting JSON with parsing settings

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
  "feed-format": "JSON",
  "feed-type": "Domain",
  "update-interval": 60,
  "json-query": ".[]|.domains",
  "use-gateway-proxy": false,
  "custom-header": [
    {
      "header-name": "new_header",
      "header-value": "new_value"
    }
  ]
}
```

## Example Responses

### Example 1: set-network-feed - JSON with parsing settings
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "847e0019-99de-42ec-ac31-56796363e019",
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
      "posix": 1637658589580,
      "iso-8601": "2021-11-23T11:09+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1637658293324,
      "iso-8601": "2021-11-23T11:04+0200"
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
  "fields-delimiter": "",
  "use-gateway-proxy": false,
  "certificate-id": "",
  "update-interval": 60,
  "data-column": 1,
  "feed-format": "JSON",
  "feed-type": "Domain",
  "json-query": ".[]|.domains",
  "custom-headers": [
    {
      "headerName": "new_header",
      "headerValue": "new_value"
    }
  ],
  "ignore-lines-that-start-with": "#"
}
```
