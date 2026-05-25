# set-threat-profile (replace-clear all overrides)

**Collection:** Web API (version 2.1) > 117 Threat Profile
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-threat-profile`

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
  "overrides": []
}
```

## Example Responses

### Example 1: set-threat-profile (replace-clear all overrides)
**Status:** `200 OK`
