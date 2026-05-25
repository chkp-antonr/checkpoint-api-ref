# show voip-domain-h323-gatekeepers

**Collection:** Web API (version 2.1) > 28 VoIP Domain H.323 Gatekeeper
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-voip-domain-h323-gatekeepers`

## Description

Show all existing voip domain h323 gatekeepers

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

### Example 1: show voip-domain-h323-gatekeepers
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 2,
  "total": 2,
  "objects": [
    {
      "uid": "6b5beb1d-8332-4cf8-b7f8-4598bbb2c10d",
      "name": "vdhg1",
      "type": "voip-domain-h323-gatekeeper",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "NetworkObjects/VoIPGatekeeper",
      "color": "black"
    },
    {
      "uid": "f36648cf-8b90-475d-a224-364c2ac80204",
      "name": "vdhg1_Clone",
      "type": "voip-domain-h323-gatekeeper",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "NetworkObjects/VoIPGatekeeper",
      "color": "black"
    }
  ]
}
```
