# show-radius-servers

**Collection:** Web API (version 2.1) > 32 RADIUS Server
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-radius-servers`

## Description

Show radius servers

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "limit": 4,
  "offset": 0,
  "details-level": "standard"
}
```

## Example Responses

### Example 1: show-radius-servers
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 4,
  "total": 16,
  "objects": [
    {
      "uid": "827e2bd0-5a6f-4284-a311-55dedb0b7b55",
      "name": "jlt58756584",
      "type": "radius-server",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "Objects/account_unit",
      "color": "black"
    },
    {
      "uid": "bcd24f54-b54d-4d56-94e7-faff5c2ca0ae",
      "name": "jlt844",
      "type": "radius-server",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "Objects/account_unit",
      "color": "black"
    },
    {
      "uid": "e7484d29-ae83-4a84-b0ed-c3db9b129234",
      "name": "jlt8584",
      "type": "radius-server",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "Objects/account_unit",
      "color": "black"
    },
    {
      "uid": "9004901b-0ea2-4918-983a-a1f6b162ba8a",
      "name": "jlt858444",
      "type": "radius-server",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "Objects/account_unit",
      "color": "black"
    }
  ]
}
```
