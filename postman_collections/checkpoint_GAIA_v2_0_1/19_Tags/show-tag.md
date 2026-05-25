# show-tag

**Collection:** Web API (version 2.0.1) > 19 Tags
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-tag`

## Description

Show tag

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "f96b37ec-e22e-4945-8bbf-d37b117914e0"
}
```

## Example Responses

### Example 1: show-tag
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "f96b37ec-e22e-4945-8bbf-d37b117914e0",
  "folder": {
    "uid": "a25a7783-9adb-4a65-9850-b97ee7860530",
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
      "posix": 1432132263822,
      "iso-8601": "2015-05-20T17:31+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1432132263822,
      "iso-8601": "2015-05-20T17:31+0300"
    },
    "creator": "aa"
  },
  "tags": [],
  "name": "my tag",
  "comments": "",
  "color": "black",
  "icon": "General/globalsNa"
}
```
