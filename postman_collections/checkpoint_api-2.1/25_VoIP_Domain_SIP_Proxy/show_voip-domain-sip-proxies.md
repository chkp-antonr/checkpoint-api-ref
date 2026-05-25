# show voip-domain-sip-proxies

**Collection:** Web API (version 2.1) > 25 VoIP Domain SIP Proxy
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-voip-domain-sip-proxies`

## Description

Retrieve all voip domain sip proxies.

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

### Example 1: show voip-domain-sip-proxies
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 2,
  "total": 2,
  "objects": [
    {
      "uid": "538b8046-d50c-4d09-93a4-92a7fe0329a5",
      "name": "sip1",
      "type": "voip-domain-sip-proxy",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "NetworkObjects/VoIPSIP",
      "color": "black"
    },
    {
      "uid": "baabb858-050f-4036-8a8e-eaf55898eb5d",
      "name": "sip1_Clone",
      "type": "voip-domain-sip-proxy",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "NetworkObjects/VoIPSIP",
      "color": "black"
    }
  ]
}
```
