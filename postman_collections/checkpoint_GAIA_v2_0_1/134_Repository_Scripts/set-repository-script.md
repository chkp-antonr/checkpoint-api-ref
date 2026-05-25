# set-repository-script

**Collection:** Web API (version 2.0.1) > 134 Repository Scripts
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-repository-script`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Script 1",
  "script-body": "cpstat os -f all",
  "color": "green"
}
```

## Example Responses

### Example 1: set-repository-script
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "cd080d1b-62b0-4ef0-b2dc-61798fff5aa3",
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
      "posix": 1645455592594,
      "iso-8601": "2022-02-21T16:40+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1645455592594,
      "iso-8601": "2022-02-21T16:40+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": "true",
  "comments": "",
  "color": "light green",
  "icon": "General/Script",
  "script-body": "cpstat os -f all"
}
```
