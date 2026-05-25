# clone-tag

**Collection:** Web API (version 2.1) > 19 Tags
**Method:** `POST`
**URL:** `{{server}}/v2.1/clone-tag`

## Description

Clone existing tag.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "My New Tag1"
}
```

## Example Responses

### Example 1: clone-tag
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "81e701ad-8f59-4e9f-9bb4-4b226ae0e67b",
  "name": "My New Tag1_Clone",
  "type": "tag",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1747411560600,
      "iso-8601": "2025-05-16T19:06+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1747411560600,
      "iso-8601": "2025-05-16T19:06+0300"
    },
    "creator": "WEB_API"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Tags/Tag"
}
```
