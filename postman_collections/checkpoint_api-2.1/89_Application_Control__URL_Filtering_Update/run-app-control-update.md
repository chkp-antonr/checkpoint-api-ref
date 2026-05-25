# run-app-control-update

**Collection:** Web API (version 2.1) > 89 Application Control & URL Filtering Update
**Method:** `POST`
**URL:** `{{server}}/v2.1/run-app-control-update`

## Description

Run Application Control & URL Filtering update

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

### Example 1: run-app-control-update
**Status:** `200 OK`

**Body:**
```javascript
{
  "tasks": [
    {
      "uid": "292a7c0f-4b42-4cb3-97ea-186b411e1199",
      "type": "task",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "meta-info": {
        "lock": "unlocked",
        "validation-state": "ok",
        "last-modify-time": {
          "posix": 1735822160024,
          "iso-8601": "2025-01-02T14:49+0200"
        },
        "last-modifier": "System",
        "creation-time": {
          "posix": 1735822149328,
          "iso-8601": "2025-01-02T14:49+0200"
        },
        "creator": "WEB_API"
      },
      "available-actions": {
        "edit": "true",
        "delete": "true",
        "clone": "false"
      },
      "tags": [],
      "read-only": false,
      "comments": "The applications are up-to-date.",
      "color": "black",
      "icon": "General/globalsNa",
      "task-name": "Application Control & URL Filtering",
      "task-id": "b28b2960-effc-4d46-b7cb-3ce7b0bfda38",
      "status": "succeeded",
      "progress-percentage": 100,
      "start-time": {
        "posix": 1735822149311,
        "iso-8601": "2025-01-02T14:49+0200"
      },
      "last-update-time": {
        "posix": 1735822160007,
        "iso-8601": "2025-01-02T14:49+0200"
      },
      "suppressed": false,
      "task-details": [
        {
          "uid": "c02250e8-6c85-4db7-801e-83bd863232d7",
          "domain": {
            "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
            "name": "SMC User",
            "domain-type": "domain"
          },
          "color": "black",
          "statusCode": "succeeded",
          "statusDescription": "The applications are up-to-date.",
          "taskNotification": "292a7c0f-4b42-4cb3-97ea-186b411e1199",
          "meta-info": {
            "validation-state": "ok",
            "last-modify-time": {
              "posix": 1735822160037,
              "iso-8601": "2025-01-02T14:49+0200"
            },
            "last-modifier": "System",
            "creation-time": {
              "posix": 1735822149376,
              "iso-8601": "2025-01-02T14:49+0200"
            },
            "creator": "WEB_API"
          },
          "tags": [],
          "icon": "General/globalsNa",
          "comments": "",
          "display-name": ""
        }
      ]
    }
  ]
}
```
