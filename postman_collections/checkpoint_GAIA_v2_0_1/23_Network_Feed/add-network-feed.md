# add-network-feed

**Collection:** Web API (version 2.0.1) > 23 Network Feed
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-network-feed`

## Description

Adding a Network Feed

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
  "feed-url": "https://www.feedsresource.com/resource"
}
```

## Example Responses

### Example 1: add-network-feed
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "5aa19932-0649-4ed8-9e98-ad9be1ecb9f2",
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
      "posix": 1627301945741,
      "iso-8601": "2021-07-26T15:19+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1627301945741,
      "iso-8601": "2021-07-26T15:19+0300"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/NetworkFeed",
  "feed-url": "https://www.feedsresource.com/resource",
  "username": "",
  "fields-delimiter": "\n",
  "use-gateway-proxy": true,
  "certificate-id": "",
  "update-interval": 60,
  "feed-format": "Flat List",
  "feed-type": "IP Address",
  "data-column": 1,
  "custom-headers": [],
  "ignore-lines-that-start-with": "#"
}
```
