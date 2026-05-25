# add-smart-task that sends a web request via proxy after policy installations

**Collection:** Web API (version 2.1) > 143 SmartTasks
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-smart-task`

## Description

Adds a SmartTask that will run after install policy and send a web request to the target URL via the specified proxy.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "Send Policy Installation Reports via Proxy",
  "description": "Send policy installation results to the mail address specified in the Custom Data field using the corporate's dedicated web server.",
  "enabled": true,
  "trigger": "After Install Policy",
  "custom-data": "{\"mail-address\": \"example-admin@example-corp.com\"}",
  "action": {
    "send-web-request": {
      "url": "https://demo.example-corp.com/policy-installation-reports/",
      "override-proxy": true,
      "proxy-url": "http://proxy.example-corp.com:8080",
      "shared-secret": "mysharedsecret1",
      "time-out": 60
    }
  }
}
```

## Example Responses

### Example 1: add-smart-task that sends a web request via proxy after policy installations
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "19c71ca2-3080-4617-b6ea-7c376e582bb8",
  "name": "Send Policy Installation Reports",
  "type": "smart-task",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1556717294959,
      "iso-8601": "2019-05-01T16:28+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1556717294959,
      "iso-8601": "2019-05-01T16:28+0300"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/SmartTask",
  "enabled": true,
  "trigger": {
    "uid": "2f98776f-1352-4947-a087-0446d8b5d93c",
    "name": "After Install Policy",
    "type": "smart-task-trigger",
    "domain": {
      "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
      "name": "Check Point Data",
      "domain-type": "data domain"
    }
  },
  "description": "Send policy installation results to the mail address specified in the Custom Data field using the corporate's dedicated web server.",
  "fail-open": true,
  "custom-data": "{\"mail-address\": \"example-admin@example-corp.com\"}",
  "action": {
    "web-request": {
      "url": "https://demo.example.com/policy-installation-reports/",
      "time-out": 30000
    }
  }
}
```
