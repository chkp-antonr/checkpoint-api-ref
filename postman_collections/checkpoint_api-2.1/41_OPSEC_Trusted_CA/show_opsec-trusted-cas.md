# show opsec-trusted-cas

**Collection:** Web API (version 2.1) > 41 OPSEC Trusted CA
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-opsec-trusted-cas`

## Description

Show opsec trusted cas

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{}
```

## Example Responses

### Example 1: show opsec-trusted-cas
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 2,
  "total": 2,
  "objects": [
    {
      "uid": "24dfc6a6-a0a3-4d12-90e5-295d9790f3b9",
      "name": "opsec_ca",
      "type": "opsec-trusted-ca",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "Objects/account_unit",
      "color": "black"
    },
    {
      "uid": "325aabc3-dd0b-4da8-b015-44cb0f4ce5c3",
      "name": "opsec_ca2",
      "type": "opsec-trusted-ca",
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
