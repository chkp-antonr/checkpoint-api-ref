# set-compliance-settings

**Collection:** Web API (version 2.1) > 71 Settings
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-compliance-settings`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "automatic-scan-scheduler.scheduled-scan-on": false,
  "automatic-scan-scheduler.scan-day": "sunday",
  "automatic-scan-scheduler.scan-time": "08:00:00",
  "partial-scan-delay": -1
}
```

## Example Responses

### Example 1: set-compliance-settings
**Status:** `200 OK`

**Body:**
```javascript
{
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "initialize-best-practices": false,
  "partial-scan-delay": -1,
  "automatic-scan-scheduler": {
    "scheduled-scan-on": false,
    "scan-day": "sunday",
    "scan-time": "08:00:00"
  },
  "enable-smart-event-logs": true,
  "enable-email-alerts": true
}
```
