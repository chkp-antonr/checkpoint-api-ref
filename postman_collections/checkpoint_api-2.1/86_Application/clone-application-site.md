# clone-application-site

**Collection:** Web API (version 2.1) > 86 Application
**Method:** `POST`
**URL:** `{{server}}/v2.1/clone-application-site`

## Description

Clone existing application site

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Application Site 1"
}
```

## Example Responses

### Example 1: clone-application-site
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "e5422095-cbf3-44f1-b71d-7cf0210b00ad",
  "name": "New Application Site 1_Clone",
  "type": "application-site",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1747514114760,
      "iso-8601": "2025-05-17T23:35+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1747514114760,
      "iso-8601": "2025-05-17T23:35+0300"
    },
    "creator": "WEB_API"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/application",
  "groups": [],
  "application-id": 1376284079,
  "primary-category": "Social Networking",
  "primary-category-id": "00fa9e44-4165-0f65-e053-08241dc22da2",
  "description": "My Application Site",
  "risk": "Unknown",
  "user-defined": true,
  "additional-categories": [
    "New Application Site Category 1"
  ],
  "additional-categories-ids": [
    "40ea63ba-5d27-4269-b5de-ac8e6910872e"
  ],
  "url-list": [
    "www.cnet.com",
    "www.stackoverflow.com"
  ],
  "urls-defined-as-regular-expression": false
}
```
