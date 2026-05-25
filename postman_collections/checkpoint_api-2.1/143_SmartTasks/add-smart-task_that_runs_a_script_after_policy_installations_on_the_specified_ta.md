# add-smart-task that runs a script after policy installations on the specified targets

**Collection:** Web API (version 2.1) > 143 SmartTasks
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-smart-task`

## Description

Adds a SmartTask that will run after policy installations and execute the "Show Policy Status" script on the specified targets.<br>Note:<br>This example assumes a script called "Show Policy Status" exists in the Management's Script Repository.<br>The Script Repository can be accessed from SmartConsole > Gateways & Servers > Scripts > Script Repository

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "Show Policy Status on Gateways",
  "trigger": "After Install Policy",
  "description": "Run policy status script on gateways after policy installations.",
  "action": {
    "run-script": {
      "repository-script": "Show Policy Status",
      "targets": [
        "Corporate-Gateway",
        "BranchOffice"
      ],
      "time-out": 120
    }
  },
  "enabled": true
}
```

## Example Responses

### Example 1: add-smart-task that runs a script after policy installations on the specified targets
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "37a1a743-3f76-41cc-bc71-2ff2c0dd8da3",
  "name": "Validate Session Name Before Publish",
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
      "posix": 1563808879731,
      "iso-8601": "2019-07-22T18:21+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1563808879731,
      "iso-8601": "2019-07-22T18:21+0300"
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
    "uid": "c1ae2fc1-aeda-413a-9910-f9083f9885fa",
    "name": "Before Publish",
    "type": "smart-task-trigger",
    "domain": {
      "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
      "name": "Check Point Data",
      "domain-type": "data domain"
    }
  },
  "description": "Run a validation script that ensures that the a session name matches the expected name format as described in the Custom Data field.",
  "fail-open": true,
  "custom-data": "{\"session-name-format\": \"CR\"}",
  "action": {
    "run-script": {
      "repository-script": {
        "uid": "ce47e4ce-7dbb-45fa-8025-b16af0fa9a53",
        "name": "Session Name Validation Script",
        "type": "Script",
        "domain": {
          "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
          "name": "SMC User",
          "domain-type": "domain"
        }
      }
    }
  }
}
```
