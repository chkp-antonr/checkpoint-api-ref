# Install LSM Policy

**Collection:** Web API (version 2.0.1) > 159 Provisioning
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/install-lsm-policy`

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

### Example 1: Install LSM Policy
**Status:** `200 OK`

**Body:**
```javascript
{
  "tasks": [
    {
      "task-id": "01234567-89ab-cdef-ba25-aabdd03256ec",
      "task-name": "Run Command operation",
      "status": "succeeded",
      "progress-percentage": 100,
      "suppressed": false,
      "task-details": [
        {
          "title": "Run command Install LSM Policy succeeded",
          "target": "lsm_gateway",
          "messages": [
            "The action has been completed successfully."
          ]
        }
      ]
    }
  ]
}
```
