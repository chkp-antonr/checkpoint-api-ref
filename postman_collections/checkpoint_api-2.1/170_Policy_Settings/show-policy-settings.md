# show-policy-settings

**Collection:** Web API (version 2.1) > 170 Policy Settings
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-policy-settings`

## Description

Show Policy settings

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{}
```

## Example Responses

### Example 1: show-policy-settings
**Status:** `200 OK`

**Body:**
```javascript
{
  "security-access-defaults": {
    "source": "any",
    "destination": "any",
    "service": "any",
    "track": "none"
  },
  "last-in-cell": "restore to default",
  "none-object-behavior": "none",
  "log-generation": "standard"
}
```
