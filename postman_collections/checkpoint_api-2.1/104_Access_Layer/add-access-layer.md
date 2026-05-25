# add-access-layer

**Collection:** Web API (version 2.1) > 104 Access Layer
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-access-layer`

## Description

Add access layer

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Layer 1"
}
```

## Example Responses

### Example 1: add-access-layer
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "81530aad-bc98-4e8f-a62d-079424ddd955",
  "folder": {
    "uid": "3b1764a5-363a-4f63-a2ab-2ef90746c70c",
    "name": "/Global Objects"
  },
  "domain": {
    "domain-type": "local domain",
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User"
  },
  "meta-info": {
    "lock": "locked by current session",
    "validation-state": "ok",
    "read-only": false,
    "last-modify-time": {
      "posix": 1435737909731,
      "iso-8601": "2015-07-01T11:05+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1435737908063,
      "iso-8601": "2015-07-01T11:05+0300"
    },
    "creator": "aa"
  },
  "tags": [],
  "name": "New Layer 1",
  "comments": "",
  "color": "black",
  "icon": "ApplicationFirewall/rulebase",
  "applications-and-url-filtering": false,
  "data-awareness": false,
  "mobile-access": false,
  "show-parent-rule": true,
  "dynamic-layer": false
}
```
