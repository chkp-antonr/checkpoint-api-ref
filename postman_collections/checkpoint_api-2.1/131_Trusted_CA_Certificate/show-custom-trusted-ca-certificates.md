# show-custom-trusted-ca-certificates

**Collection:** Web API (version 2.1) > 131 Trusted CA Certificate
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-custom-trusted-ca-certificates`

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

### Example 1: show-custom-trusted-ca-certificates
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 1,
  "total": 1,
  "objects": [
    {
      "uid": "f6afaa0f-f978-4b1c-8575-6cbc9459af11",
      "name": "CA_F6AFAA0F_F978_4B1C_8575_6CBC9459AF11",
      "type": "custom-trusted-ca-certificate",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "General/globalsNa",
      "color": "black"
    }
  ]
}
```
