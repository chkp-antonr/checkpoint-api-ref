# add-script encoded in base64

**Collection:** Web API (version 2.0.1) > 134 Repository Scripts
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-repository-script`

## Description

Adds a simple repository script in base64

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "Script Example: List files under / dir",
  "script-body-base64": "bHMgLWwgLw=="
}
```

## Example Responses

### Example 1: add-script encoded in base64
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "870e6432-a38f-4d8f-8d72-e13d7c5061ca",
  "name": "New Script 1",
  "type": "repository-script",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1645454571940,
      "iso-8601": "2022-02-21T16:42+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1645454571940,
      "iso-8601": "2022-02-21T16:42+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": "true",
  "comments": "",
  "color": "black",
  "icon": "General/Script",
  "script-body": "ls -l /"
}
```
