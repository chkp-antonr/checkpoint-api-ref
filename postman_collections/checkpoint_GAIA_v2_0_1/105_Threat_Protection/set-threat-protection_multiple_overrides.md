# set-threat-protection (multiple overrides)

**Collection:** Web API (version 2.0.1) > 105 Threat Protection
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-threat-protection`

## Description

Sets overrides to existing profiles for a specific protection.<br>In the example below, two overrides will be set, one for "New Profile 1" and a second one for "New Profile 2".

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "FTP Commands",
  "overrides": [
    {
      "profile": "New Profile 1",
      "action": "inactive",
      "track": "Log",
      "capture-packets": true
    },
    {
      "profile": "New Profile 2",
      "action": "inactive",
      "track": "Log",
      "capture-packets": true
    }
  ]
}
```

## Example Responses

### Example 1: set-threat-protection (multiple overrides)
**Status:** `200 OK`
