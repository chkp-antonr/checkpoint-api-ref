# get-interfaces without topology by UID

**Collection:** Web API (version 2.1) > 64 Network Interface
**Method:** `POST`
**URL:** `{{server}}/v2.1/get-interfaces`

## Description

Get interfaces without topology from target gateway or cluster by UID

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "target-uid": "2220d9ad-a251-5555-9a0a-4772a6511111",
  "with-topology": false
}
```

## Example Responses

### Example 1: get-interfaces without topology by UID
**Status:** `200 OK`

**Body:**
```javascript
{
  "tasks": [
    {
      "task-name": "get-interfaces",
      "task-id": "01234567-89ab-cdef-9e1f-0e1e68312345",
      "status": "succeeded",
      "progress-percentage": 100,
      "suppressed": false,
      "task-details": [
        {
          "interfaces": [
            "eth0",
            "eth1"
          ]
        }
      ]
    }
  ]
}
```
