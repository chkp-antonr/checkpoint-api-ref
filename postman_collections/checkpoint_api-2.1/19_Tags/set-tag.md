# set-tag

**Collection:** Web API (version 2.1) > 19 Tags
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-tag`

## Description

Set tag

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
  "new-name": "My New Tag21",
  "tags": {
    "add": "tag3"
  }
}
```

## Example Responses

### Example 1: set-tag
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
      "posix": 1432132678015,
      "iso-8601": "2015-05-20T17:37+0300"
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
      "name": "tag3",
      "uid": "dda885bb-0d5b-4529-96eb-55b757847092"
    }
  ],
  "name": "My New Tag21",
  "comments": "",
  "color": "black",
  "icon": "General/globalsNa"
}
```
