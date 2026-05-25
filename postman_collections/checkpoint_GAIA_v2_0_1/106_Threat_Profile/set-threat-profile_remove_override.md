# set-threat-profile (remove override)

**Collection:** Web API (version 2.0.1) > 106 Threat Profile
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-threat-profile`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Profile 2",
  "comments": "update recommended profile  ",
  "active-protections-performance-impact": "low",
  "active-protections-severity": "low or above",
  "confidence-level-medium": "prevent",
  "confidence-level-high": "prevent",
  "threat-emulation": true,
  "anti-virus": false,
  "anti-bot": true,
  "ips": false,
  "overrides": {
    "remove": [
      "VNC"
    ]
  }
}
```

## Example Responses

### Example 1: set-threat-profile (remove override)
**Status:** `200 OK`
