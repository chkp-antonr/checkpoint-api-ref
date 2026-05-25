# set-cp-password-requirements

**Collection:** Web API (version 2.1) > 165 Check Point Password Requirements
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-cp-password-requirements`

## Description

Edit Check point password requirements.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "min-password-length": 7
}
```

## Example Responses

### Example 1: set-cp-password-requirements
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "02ddac95-d8aa-4db0-bb4a-bdcbb6e98e4f",
  "type": "cp-password-requirements",
  "domain": {
    "uid": "a0eebc99-afed-4ef8-bb6d-fedfedfedfed",
    "name": "System Data",
    "domain-type": "mds"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1738765682797,
      "iso-8601": "2025-02-05T16:28+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1738588308551,
      "iso-8601": "2025-02-03T15:11+0200"
    },
    "creator": "System"
  },
  "min-password-length": 7
}
```
