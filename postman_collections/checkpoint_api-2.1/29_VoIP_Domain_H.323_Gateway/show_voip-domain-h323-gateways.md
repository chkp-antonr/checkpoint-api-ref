# show voip-domain-h323-gateways

**Collection:** Web API (version 2.1) > 29 VoIP Domain H.323 Gateway
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-voip-domain-h323-gateways`

## Description

Show all existing voip domain h323 gateways

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "limit": 5,
  "offset": 0
}
```

## Example Responses

### Example 1: show voip-domain-h323-gateways
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 2,
  "total": 2,
  "objects": [
    {
      "uid": "41e4af63-5c3f-4fef-a5a3-138e33a1c08a",
      "name": "vdhgw1",
      "type": "voip-domain-h323-gateway",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "NetworkObjects/VoIPGateway",
      "color": "black"
    },
    {
      "uid": "2972a79c-6b90-4875-a528-8c1826450804",
      "name": "vdhgw1_Clone",
      "type": "voip-domain-h323-gateway",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "NetworkObjects/VoIPGateway",
      "color": "black"
    }
  ]
}
```
