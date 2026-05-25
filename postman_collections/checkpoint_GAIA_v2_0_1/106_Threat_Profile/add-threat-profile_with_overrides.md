# add-threat-profile (with overrides)

**Collection:** Web API (version 2.0.1) > 106 Threat Profile
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-threat-profile`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Profile 1",
  "active-protections-performance-impact": "low",
  "active-protections-severity": "low or above",
  "confidence-level-medium": "prevent",
  "confidence-level-high": "prevent",
  "threat-emulation": true,
  "anti-virus": true,
  "anti-bot": true,
  "ips": true,
  "ips-settings": {
    "newly-updated-protections": "staging",
    "exclude-protection-with-performance-impact": true,
    "exclude-protection-with-performance-impact-mode": "High or lower"
  },
  "overrides": [
    {
      "protection": "VNC",
      "capture-packets": true,
      "action": "Prevent",
      "track": "Log"
    },
    {
      "protection": "GoToMyPC",
      "capture-packets": true,
      "action": "Prevent",
      "track": "Log"
    }
  ]
}
```

## Example Responses

### Example 1: add-threat-profile (with overrides)
**Status:** `200 OK`
