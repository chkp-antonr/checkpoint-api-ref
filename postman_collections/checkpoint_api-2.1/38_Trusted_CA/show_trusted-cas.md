# show trusted-cas

**Collection:** Web API (version 2.1) > 38 Trusted CA
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-trusted-cas`

## Description

Show trusted cas

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

### Example 1: show trusted-cas
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 5,
  "total": 5,
  "objects": [
    {
      "uid": "bae2e0c7-4667-49a8-95c7-1ce9d7cd6584",
      "name": "external_ca",
      "type": "external-trusted-ca",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "Objects/account_unit",
      "color": "black"
    },
    {
      "uid": "7347edb6-8a6d-4f74-9ee2-233b7381b030",
      "name": "external_ca2",
      "type": "external-trusted-ca",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "Objects/account_unit",
      "color": "black"
    },
    {
      "uid": "c79b045c-6e2f-9e40-94d2-c86246db6ad4",
      "name": "internal_ca",
      "type": "internal-trusted-ca",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "Objects/account_unit",
      "color": "black"
    },
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
