# add objects-batch

**Collection:** Web API (version 2.1) > 184 Objects Batch
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-objects-batch`

## Description

Add two hosts and two address ranges

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
          "ip-address": "192.0.2.1"
        },
        {
          "name": "New Host 2",
          "ip-address": "192.0.2.2"
        }
      ]
    },
    {
      "type": "address-range",
      "list": [
        {
          "name": "New Address Range 1",
          "ip-address-first": "192.0.2.1",
          "ip-address-last": "192.0.2.10"
        },
        {
          "name": "New Address Range 2",
          "ip-address-first": "192.0.2.12",
          "ip-address-last": "192.0.2.20"
        }
      ]
    }
  ]
}
```

## Example Responses

### Example 1: add objects-batch
**Status:** `200 OK`

**Body:**
```javascript
{
  "tasks": [
    {
      "task-name": "add-objects-batch",
      "task-id": "abcdef01-2345-6789-b3e1-ec3bf46e688a",
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
