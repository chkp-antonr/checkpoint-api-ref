# add-dynamic-object

**Collection:** Web API (version 2.0.1) > 18 Dynamic Object
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-dynamic-object`

## Description

Adds new dynamic object

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "Dynamic_Object_1",
  "comments": "My Dynamic Object 1",
  "color": "yellow"
}
```

## Example Responses

### Example 1: add-dynamic-object
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "c5a7f50c-a951-45be-8b82-48441c9f48de",
  "name": "Dynamic_Object_1",
  "type": "dynamic-object",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1478597722485,
      "iso-8601": "2016-11-08T11:35+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1478597722485,
      "iso-8601": "2016-11-08T11:35+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "My Dynamic Object 1",
  "color": "yellow",
  "icon": "NetworkObjects/dynamicObject"
}
```
