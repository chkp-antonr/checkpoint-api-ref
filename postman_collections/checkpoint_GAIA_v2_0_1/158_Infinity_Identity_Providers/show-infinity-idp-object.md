# show-infinity-idp-object

**Collection:** Web API (version 2.0.1) > 158 Infinity Identity Providers
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-infinity-idp-object`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "User1"
}
```

## Example Responses

### Example 1: show-infinity-idp-object
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "7766434f-6b81-4047-8fd3-05d7f1e0a867",
  "name": "Ofri Shani",
  "type": "InfinityIdpUser",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1697981245448,
      "iso-8601": "2023-10-22T16:27+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1697981245448,
      "iso-8601": "2023-10-22T16:27+0300"
    },
    "creator": "aa"
  },
  "icon": "Objects/user",
  "idp-id": "897d81db-721a-4531-b0e9-75ed0e951bb6",
  "idp-name": "devOkta_Infinity",
  "idp-display-name": "devOkta",
  "ext-id": "00u9hdmasbp1egl0i5d7",
  "description": "ofris@checkpoint.com",
  "display-name": "Ofri Shani",
  "object-type": "Idp User"
}
```
