# set objects-batch

**Collection:** Web API (version 2.0.1) > 166 Objects Batch
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-objects-batch`

## Description

Set two hosts and two address ranges

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "objects": [
    {
      "type": "host",
      "list": [
        {
          "name": "New Host 1",
          "ipv4-address": "192.0.2.2",
          "color": "green"
        },
        {
          "name": "New Host 2",
          "ipv4-address": "192.0.2.3",
          "color": "green"
        }
      ]
    },
    {
      "type": "address-range",
      "list": [
        {
          "name": "New Address Range 1",
          "new-name": "New Address Range 3",
          "color": "green",
          "ip-address-first": "192.0.2.1",
          "ip-address-last": "192.0.2.1"
        },
        {
          "name": "New Address Range 2",
          "new-name": "New Address Range 4",
          "color": "green",
          "ip-address-first": "192.0.2.2",
          "ip-address-last": "192.0.2.2"
        }
      ]
    }
  ]
}
```

## Example Responses

### Example 1: set objects-batch
**Status:** `200 OK`

**Body:**
```javascript
{
  "tasks": [
    {
      "task-name": "set-objects-batch",
      "task-id": "abcdef01-2345-6789-b3e1-ec3bf46e688b",
      "status": "succeeded",
      "progress-percentage": 100,
      "progress-description": "Operation Complete",
      "suppressed": false,
      "task-details": [
        {
          "status": "Batch operation completed successfully"
        }
      ]
    }
  ]
}
```
