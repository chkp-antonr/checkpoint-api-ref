# set-threat-ioc-feed (Simple)

**Collection:** Web API (version 2.1) > 119 Threat IOC feed
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-threat-ioc-feed`

## Description

Setting a simple threat IOC feed

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "ioc_feed",
  "use-gateway-proxy": false,
  "action": "detect"
}
```

## Example Responses

### Example 1: set-threat-ioc-feed (Simple)
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "eb3040f5-f2e5-46b0-96fa-f72dc2520d3d",
  "name": "ioc_feed",
  "type": "threat-ioc-feed",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1642672860013,
      "iso-8601": "2022-01-20T12:01+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1642672816479,
      "iso-8601": "2022-01-20T12:00+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "ThreatPrevention/FileGlobe",
  "feed-url": "https://www.feedsresource.com/resource",
  "use-gateway-proxy": false,
  "action": "Detect",
  "enabled": false,
  "use-custom-feed-settings": false,
  "custom-headers": [],
  "feed-type": "domain"
}
```
