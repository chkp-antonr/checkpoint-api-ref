# get-interfaces with topology by name

**Collection:** Web API (version 2.0.1) > 57 Network Interface
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/get-interfaces`

## Description

Get interfaces with topology from target gateway or cluster by name

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "target-name": "gw123",
  "with-topology": true
}
```

## Example Responses

### Example 1: get-interfaces with topology by name
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
