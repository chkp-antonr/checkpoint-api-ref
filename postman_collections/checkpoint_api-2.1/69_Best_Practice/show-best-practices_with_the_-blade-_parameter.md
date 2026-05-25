# show-best-practices with the "blade" parameter

**Collection:** Web API (version 2.1) > 69 Best Practice
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-best-practices`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "blade": "Anti-Bot"
}
```

## Example Responses

### Example 1: show-best-practices with the "blade" parameter
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 1,
  "total": 1,
  "objects": [
    {
      "uid": "89862757-34a9-4788-9fd4-be95b63a004d",
      "name": "Check that each Gateway's Anti-Bot configuration is activated according to the policy",
      "type": "compliance-best-practice",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "meta-info": {
        "lock": "unlocked",
        "validation-state": "ok",
        "last-modify-time": {
          "posix": 1747665996374,
          "iso-8601": "2025-05-19T17:46+0300"
        },
        "last-modifier": "System",
        "creation-time": {
          "posix": 1747665908553,
          "iso-8601": "2025-05-19T17:45+0300"
        },
        "creator": "System"
      },
      "available-actions": {
        "edit": "true",
        "delete": "true",
        "clone": "true"
      },
      "read-only": false,
      "best-practice-id": "AB104",
      "description": "This checks that each Gateway is activated according to the profiles defined in the Anti-Bot policy",
      "action-item": "Each Gateway should be configured to work according to the profiles defined in the Anti-Bot policy. The Activation Mode should be set to 'According to Policy' and not 'Detect Only'.",
      "status": "n/a",
      "blade": "anti-bot",
      "user-defined": false,
      "active": true
    }
  ]
}
```
