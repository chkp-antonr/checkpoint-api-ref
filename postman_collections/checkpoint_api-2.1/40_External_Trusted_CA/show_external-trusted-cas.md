# show external-trusted-cas

**Collection:** Web API (version 2.1) > 40 External Trusted CA
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-external-trusted-cas`

## Description

Show external trusted cas

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

### Example 1: show external-trusted-cas
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 2,
  "total": 2,
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
    }
  ]
}
```
