# set-threat-protection

**Collection:** Web API (version 2.1) > 116 Threat Protection
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-threat-protection`

## Description

Sets an override to an existing profile for a specific protection.<br>In the example below, one override will be set for "New Profile 1".

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
      "track": "None",
      "capture-packets": true
    }
  ]
}
```

## Example Responses

### Example 1: set-threat-protection
**Status:** `200 OK`
