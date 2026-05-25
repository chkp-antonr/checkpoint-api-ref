# show-threat-ioc-feed

**Collection:** Web API (version 2.1) > 119 Threat IOC feed
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-threat-ioc-feed`

## Description

Showing a threat IOC feed

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "ioc_feed"
}
```

## Example Responses

### Example 1: show-threat-ioc-feed
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "398986f2-ee71-4c35-b7dd-b8dd5f720451",
  "name": "ioc_feed",
  "type": "threat-ioc-feed",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "locked by current session",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1588430122224,
      "iso-8601": "2020-05-02T17:35+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1588430063560,
      "iso-8601": "2020-05-02T17:34+0300"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "ThreatPrevention/FileGlobe",
  "action": "Prevent",
  "enabled": true,
  "fields_delimiter": ",",
  "feed_url": "https://www.feedsresource.com/resource",
  "use_gateway_proxy": false,
  "use_custom_feed_settings": false,
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
  "custom-name": "1",
  "custom-value": "2",
  "custom-comment": "4",
  "custom-confidence": "3",
  "custom-severity": "5",
  "custom-type": "6",
  "feed-type": "any type",
  "ignore_lines_that_start_with": "!"
}
```
