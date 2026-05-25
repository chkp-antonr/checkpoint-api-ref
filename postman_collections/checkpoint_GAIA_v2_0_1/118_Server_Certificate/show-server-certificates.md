# show-server-certificates

**Collection:** Web API (version 2.0.1) > 118 Server Certificate
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-server-certificates`

## Description

Show all server certificates objects.

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

### Example 1: show-server-certificates
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 1,
  "total": 1,
  "objects": [
    {
      "uid": "85944ed6-fa09-40c9-ada9-d980a1dc3f3c",
      "name": "MyServerCertificate",
      "type": "server-certificate",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "subject_user_certificate",
      "color": "black"
    }
  ]
}
```
