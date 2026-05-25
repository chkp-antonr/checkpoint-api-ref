# show voip-domain-sccp-call-managers

**Collection:** Web API (version 2.1) > 27 VoIP Domain SCCP Call Manager
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-voip-domain-sccp-call-managers`

## Description

Retrieve all voip domain sccp call managers.

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

### Example 1: show voip-domain-sccp-call-managers
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 2,
  "total": 2,
  "objects": [
    {
      "uid": "02865dda-4985-4182-b528-5f7b25a43c66",
      "name": "sccp1",
      "type": "voip-domain-sccp-call-manager",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "NetworkObjects/VoIPSCCPCallManager",
      "color": "black"
    },
    {
      "uid": "08411e0b-2c25-4fbd-bbed-790925396207",
      "name": "sccp1_Clone",
      "type": "voip-domain-sccp-call-manager",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "NetworkObjects/VoIPSCCPCallManager",
      "color": "black"
    }
  ]
}
```
