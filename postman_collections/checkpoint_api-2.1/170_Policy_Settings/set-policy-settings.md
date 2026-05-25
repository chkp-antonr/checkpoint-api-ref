# set-policy-settings

**Collection:** Web API (version 2.1) > 170 Policy Settings
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-policy-settings`

## Description

Set Policy settings

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "security-access-defaults": {
    "source": "none",
    "destination": "none",
    "service": "none",
    "track": "log"
  },
  "last-in-cell": "none",
  "none-object-behavior": "warning",
  "log-generation": "aggregated"
}
```

## Example Responses

### Example 1: set-policy-settings
**Status:** `200 OK`

**Body:**
```javascript
{
  "security-access-defaults": {
    "source": "none",
    "destination": "none",
    "service": "none",
    "track": "log"
  },
  "last-in-cell": "none",
  "none-object-behavior": "warning",
  "log-generation": "aggregated"
}
```
