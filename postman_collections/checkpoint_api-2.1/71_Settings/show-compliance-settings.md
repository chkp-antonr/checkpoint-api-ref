# show-compliance-settings

**Collection:** Web API (version 2.1) > 71 Settings
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-compliance-settings`

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

### Example 1: show-compliance-settings
**Status:** `200 OK`

**Body:**
```javascript
{
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "partial-scan-delay": 0,
  "automatic-scan-scheduler": {
    "scheduled-scan-on": true,
    "scan-day": "every day",
    "scan-time": "23:59:59"
  },
  "enable-smart-event-logs": true,
  "enable-email-alerts": true,
  "initialize-best-practices": true
}
```
