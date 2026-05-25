# show-cp-trusted-ca-certificates

**Collection:** Web API (version 2.0.1) > 120 Trusted CA Certificate
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-cp-trusted-ca-certificates`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "limit": "3",
  "order.1.ASC": "status"
}
```

## Example Responses

### Example 1: show-cp-trusted-ca-certificates
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 3,
  "total": 361,
  "objects": [
    {
      "uid": "c7253c5f-5881-4d4a-b82b-f111b2182403",
      "name": "CA_0090EA36_7A7C_42DF_93EE_CFE97D542FFB",
      "type": "custom-trusted-ca-certificate",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "Unknown",
      "color": "black"
    },
    {
      "uid": "63147e3a-4553-4fa4-914c-9aeaf56fc97d",
      "name": "CA_00DCAF98_D5E7_488F_B2C2_998CFEF8E49A",
      "type": "custom-trusted-ca-certificate",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "Unknown",
      "color": "black"
    },
    {
      "uid": "53df6e19-391e-4379-9f99-b80428f01803",
      "name": "CA_00E044DC_6CF8_472D_97E4_31D8AF0F4F40",
      "type": "custom-trusted-ca-certificate",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "Unknown",
      "color": "black"
    }
  ]
}
```
