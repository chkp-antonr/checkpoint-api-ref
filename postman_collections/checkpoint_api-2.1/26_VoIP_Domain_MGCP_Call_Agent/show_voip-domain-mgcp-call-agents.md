# show voip-domain-mgcp-call-agents

**Collection:** Web API (version 2.1) > 26 VoIP Domain MGCP Call Agent
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-voip-domain-mgcp-call-agents`

## Description

Retrieve all voip domain mgcp call agents.

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

### Example 1: show voip-domain-mgcp-call-agents
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 2,
  "total": 2,
  "objects": [
    {
      "uid": "17d1a265-0eb9-4bfe-8b9c-031cac81aced",
      "name": "mgcp1",
      "type": "voip-domain-mgcp-call-agent",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "NetworkObjects/VoIPMGCPCallAgent",
      "color": "black"
    },
    {
      "uid": "0f8a36e1-3a1d-421f-a075-63b16734c919",
      "name": "mgcp1_Clone",
      "type": "voip-domain-mgcp-call-agent",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "NetworkObjects/VoIPMGCPCallAgent",
      "color": "black"
    }
  ]
}
```
