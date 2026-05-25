# show-infinity-idp

**Collection:** Web API (version 2.0.1) > 158 Infinity Identity Providers
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-infinity-idp`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "infinityIdp1"
}
```

## Example Responses

### Example 1: show-infinity-idp
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "a0e2d43d-35ba-4500-8c2f-7ee877adb36a",
  "name": "Azure1_Infinity",
  "type": "infinity-idp",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1697973710817,
      "iso-8601": "2023-10-22T14:21+0300"
    },
    "last-modifier": "System",
    "creation-time": {
      "posix": 1697973710817,
      "iso-8601": "2023-10-22T14:21+0300"
    },
    "creator": "System"
  },
  "icon": "Objects/azure",
  "idp-id": "2c1dc911-7bb0-4c79-a3b1-c62b296d8adf",
  "idp-name": "Azure1",
  "idp-type": "azure",
  "idp-domains": [
    "ofris.tk"
  ]
}
```
