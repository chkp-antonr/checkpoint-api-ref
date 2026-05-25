# run-trusted-ca-update

**Collection:** Web API (version 2.1) > 131 Trusted CA Certificate
**Method:** `POST`
**URL:** `{{server}}/v2.1/run-trusted-ca-update`

## Description

Run trusted CA update.

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

### Example 1: run-trusted-ca-update
**Status:** `200 OK`

**Body:**
```javascript
{
  "tasks": [
    {
      "uid": "e64a8a03-ff89-4610-ad0c-c324752cc040",
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
          "posix": 1746432083771,
          "iso-8601": "2025-05-05T11:01+0300"
        },
        "last-modifier": "System",
        "creation-time": {
          "posix": 1746432083493,
          "iso-8601": "2025-05-05T11:01+0300"
        },
        "creator": "aa"
      },
      "available-actions": {
        "edit": "true",
        "delete": "true",
        "clone": "false"
      },
      "tags": [],
      "read-only": false,
      "comments": "Everything is up-to-date",
      "color": "black",
      "icon": "General/globalsNa",
      "task-name": "Trusted CA's update",
      "task-id": "e00c20f3-ca29-4742-9455-3a6408ae0b05",
      "status": "succeeded",
      "progress-percentage": 100,
      "start-time": {
        "posix": 1746432083496,
        "iso-8601": "2025-05-05T11:01+0300"
      },
      "last-update-time": {
        "posix": 1746432083768,
        "iso-8601": "2025-05-05T11:01+0300"
      },
      "suppressed": false,
      "task-details": []
    }
  ]
}
```
