# show-dynamic-object

**Collection:** Web API (version 2.0.1) > 18 Dynamic Object
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-dynamic-object`

## Description

Retieves existing dynamic object

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "Dynamic_Object_1"
}
```

## Example Responses

### Example 1: show-dynamic-object
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "5d98de8f-722d-4560-ae65-829ef2bffd15",
  "name": "Dynamic_Object_1",
  "type": "dynamic-object",
  "domain": {
    "domain-type": "domain",
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User"
  },
  "meta-info": {
    "lock": "locked by current session",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1478693712579,
      "iso-8601": "2016-11-09T14:15+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1478693712579,
      "iso-8601": "2016-11-09T14:15+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": false,
  "comments": "My Dynamic Object 1",
  "color": "yellow",
  "icon": "NetworkObjects/dynamicObject"
}
```
