# set-threat-ioc-feed

**Collection:** Web API (version 2.1) > 119 Threat IOC feed
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-threat-ioc-feed`

## Description

Setting a threat IOC feed

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
  "enabled": true,
  "feed-url": "https://www.feedsresource.com/resource",
  "use-gateway-proxy": false,
  "fields-delimiter": ",",
  "ignore-lines-that-start-with": "!",
  "feed-type": "Any type",
  "action": "prevent",
  "custom-name": 1,
  "custom-value": 2,
  "custom-confidence": 3,
  "custom-comment": 4,
  "custom-severity": 5,
  "custom-type": 6,
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

### Example 1: set-threat-ioc-feed
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "0b75beaf-a789-4831-b0d6-d07535105b5f",
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
      "posix": 1642604878336,
      "iso-8601": "2022-01-19T17:07+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1642509789486,
      "iso-8601": "2022-01-18T14:43+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "ThreatPrevention/FileGlobe",
  "feed-url": "https://www.feedsresource.com/resource",
  "fields-delimiter": ",",
  "use-gateway-proxy": false,
  "action": "Prevent",
  "enabled": true,
  "use-custom-feed-settings": false,
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
  "custom-name": 1,
  "custom-value": 2,
  "custom-comment": 4,
  "custom-confidence": 3,
  "custom-severity": 5,
  "custom-type": 6,
  "feed-type": "any type",
  "ignore-lines-that-start-with": "!"
}
```
