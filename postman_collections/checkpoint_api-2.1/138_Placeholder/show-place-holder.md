# show-place-holder

**Collection:** Web API (version 2.1) > 138 Placeholder
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-place-holder`

## Description

Show rules placeholder in the global policy

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "uid": "5df27676-83a6-4d38-beaa-0413838a7f85"
}
```

## Example Responses

### Example 1: show-place-holder
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "29e05a19-d536-40af-afb2-baaf79068127",
  "folder": {
    "uid": "b21f9c05-5354-472e-a82f-e4cd6b69acc6",
    "name": "/Global Objects"
  },
  "domain": {
    "domain-type": "global domain",
    "uid": "1e294ce0-367a-11e3-aa6e-0800200c9a66",
    "name": "Global"
  },
  "meta-info": {
    "lock": "locked by current session",
    "validation-state": "ok",
    "read-only": false,
    "last-modify-time": {
      "posix": 1431609465363,
      "iso-8601": "2015-05-14T16:17+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1431609465363,
      "iso-8601": "2015-05-14T16:17+0300"
    },
    "creator": "aa"
  },
  "tags": [],
  "comments": "",
  "color": "black",
  "icon": "General/globalsNa"
}
```
