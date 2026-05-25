# add-tag

**Collection:** Web API (version 2.1) > 19 Tags
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-tag`

## Description

Add tag

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "My New Tag1",
  "tags": [
    "tag1",
    "tag2"
  ]
}
```

## Example Responses

### Example 1: add-tag
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "728a4212-a521-46a2-a5a1-b6536a9aecd5",
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
    "lock": "unlocked",
    "validation-state": "ok",
    "read-only": false,
    "last-modify-time": {
      "posix": 1432132584715,
      "iso-8601": "2015-05-20T17:36+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1432132584715,
      "iso-8601": "2015-05-20T17:36+0300"
    },
    "creator": "aa"
  },
  "tags": [
    {
      "folder": {
        "uid": "a25a7783-9adb-4a65-9850-b97ee7860530",
        "name": "/Global Objects"
      },
      "domain": {
        "domain-type": "local domain",
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User"
      },
      "type": "tag",
      "name": "tag1",
      "uid": "687715ca-674b-4642-981b-b6243fde04c0"
    },
    {
      "folder": {
        "uid": "a25a7783-9adb-4a65-9850-b97ee7860530",
        "name": "/Global Objects"
      },
      "domain": {
        "domain-type": "local domain",
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User"
      },
      "type": "tag",
      "name": "tag2",
      "uid": "f1ee4a33-6577-45da-9d4f-cc352a349c80"
    }
  ],
  "name": "My New Tag1",
  "comments": "",
  "color": "black",
  "icon": "General/globalsNa"
}
```
