# lock-object using name and type

**Collection:** Web API (version 2.1) > 183 Object
**Method:** `POST`
**URL:** `{{server}}/v2.1/lock-object`

## Description

Lock object using name and type.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "host5",
  "type": "host"
}
```

## Example Responses

### Example 1: lock-object using name and type
**Status:** `200 OK`

**Body:**
```javascript
{
  "object": {
    "uid": "03995d64-3525-4be2-993a-0a9a6294f7cb",
    "name": "host5",
    "type": "host",
    "domain": {
      "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
      "name": "SMC User",
      "domain-type": "domain"
    },
    "ipv4-address": "65.22.64.65"
  }
}
```
