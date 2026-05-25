# show-network-probes

**Collection:** Web API (version 2.1) > 110 Network Probe
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-network-probes`

## Description

Displays several Network Probes.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "limit": 50,
  "offset": 0
}
```

## Example Responses

### Example 1: show-network-probes
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 1,
  "total": 1,
  "objects": [
    {
      "uid": "6e82f8d4-9af4-4ee3-a2e2-fb45bddb0358",
      "name": "probe_GW1_http",
      "type": "network-probe",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "NetworkObjects/NetworkProbe",
      "color": "black"
    }
  ]
}
```
