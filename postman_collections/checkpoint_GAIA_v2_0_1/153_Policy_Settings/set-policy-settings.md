# set-policy-settings

**Collection:** Web API (version 2.0.1) > 153 Policy Settings
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-policy-settings`

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
    "service": "none"
  },
  "last-in-cell": "none",
  "none-object-behavior": "warning"
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
    "service": "none"
  },
  "last-in-cell": "none",
  "none-object-behavior": "warning"
}
```
