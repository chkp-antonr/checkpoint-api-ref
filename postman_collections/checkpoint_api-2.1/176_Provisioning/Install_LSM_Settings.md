# Install LSM Settings

**Collection:** Web API (version 2.1) > 176 Provisioning
**Method:** `POST`
**URL:** `{{server}}/v2.1/install-lsm-settings`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "targets": [
    "lsm_gateway"
  ]
}
```

## Example Responses

### Example 1: Install LSM Settings
**Status:** `200 OK`

**Body:**
```javascript
{
  "tasks": [
    {
      "task-id": "01234567-89ab-cdef-bb46-4530fa75c5bb",
      "task-name": "Run Command operation",
      "status": "succeeded",
      "progress-percentage": 100,
      "suppressed": false,
      "task-details": [
        {
          "title": "Run command Install LSM Settings succeeded",
          "target": "lsm_gateway",
          "messages": [
            "The action has been completed successfully"
          ]
        }
      ]
    }
  ]
}
```
