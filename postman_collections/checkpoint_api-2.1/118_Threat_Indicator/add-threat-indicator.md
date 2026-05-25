# add-threat-indicator

**Collection:** Web API (version 2.1) > 118 Threat Indicator
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-threat-indicator`

## Description

Adding a threat indicator

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "My_Indicator",
  "observables": [
    {
      "name": "My_Observable",
      "mail-to": "someone@somewhere.com",
      "confidence": "medium",
      "severity": "low",
      "product": "AV"
    }
  ],
  "action": "ask",
  "profile-overrides": [
    {
      "profile": "My_Profile",
      "action": "detect"
    }
  ],
  "ignore-warnings": true
}
```

## Example Responses

### Example 1: add-threat-indicator
**Status:** `200 OK`
