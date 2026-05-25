# set-simple-cluster change member priority

**Collection:** Web API (version 2.1) > 63 Simple Cluster
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-simple-cluster`

## Description

Change cluster member priority. Set 1 for member with highest priority. Set 3, in case of cluster with 3 members, for lowest priority member

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
  "members": {
    "update": [
      {
        "name": "mem1",
        "priority": 1
      },
      {
        "name": "mem2",
        "priority": 3
      }
    ]
  }
}
```

## Example Responses

### Example 1: set-simple-cluster change member priority
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
