# set-simple-cluster set advanced ClusterXL settings

**Collection:** Web API (version 2.0.1) > 56 Simple Cluster
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-simple-cluster`

## Description

Set ClusterXL advanced settings

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "cluster1",
  "cluster-mode": "cluster-xl-ha",
  "cluster-settings": {
    "track-changes-of-cluster-members": "alert",
    "state-synchronization": {
      "enabled": true,
      "delayed": true,
      "delayed-seconds": 5
    }
  }
}
```

## Example Responses

### Example 1: set-simple-cluster set advanced ClusterXL settings
**Status:** `200 OK`

**Body:**
```javascript
{
  "tasks": [
    {
      "task-name": "set simple-cluster",
      "task-id": "01234567-89ab-1234-8c24-e81fed34664a",
      "status": "succeeded",
      "progress-percentage": 100,
      "suppressed": false,
      "task-details": [
        {
          "message": "Successfully finished"
        }
      ]
    }
  ]
}
```
