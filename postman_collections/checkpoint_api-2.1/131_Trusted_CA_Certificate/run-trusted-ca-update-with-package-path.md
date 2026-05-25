# run-trusted-ca-update-with-package-path

**Collection:** Web API (version 2.1) > 131 Trusted CA Certificate
**Method:** `POST`
**URL:** `{{server}}/v2.1/run-trusted-ca-update`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "package-path": "/home/admin/updateFile_test.zip"
}
```

## Example Responses

### Example 1: run-trusted-ca-update-with-package-path
**Status:** `200 OK`

**Body:**
```javascript
{
  "tasks": [
    {
      "uid": "69e8ef79-b279-4c5c-a9b0-796f6f1849dd",
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
          "posix": 1746433087703,
          "iso-8601": "2025-05-05T11:18+0300"
        },
        "last-modifier": "WEB_API",
        "creation-time": {
          "posix": 1746433087703,
          "iso-8601": "2025-05-05T11:18+0300"
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
      "comments": "",
      "color": "black",
      "icon": "General/globalsNa",
      "task-name": "",
      "task-id": "356540cc-0c2c-46db-8147-0f08aa872a4b",
      "progress-percentage": 0,
      "suppressed": false,
      "task-details": []
    }
  ]
}
```
