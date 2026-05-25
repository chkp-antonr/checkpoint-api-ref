# delete rules-batch

**Collection:** Web API (version 2.1) > 185 Rules Batch
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-rules-batch`

## Description

Delete two access rules, two nat rules and two https rules

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
      "type": "access-rule",
      "layer": "Network",
      "list": [
        {
          "rule-number": 1
        },
        {
          "rule-number": 2
        }
      ]
    },
    {
      "type": "nat-rule",
      "layer": "Standard",
      "list": [
        {
          "rule-number": 1
        },
        {
          "rule-number": 2
        }
      ]
    },
    {
      "type": "https-rule",
      "layer": "Default Layer",
      "list": [
        {
          "rule-number": 1
        },
        {
          "rule-number": 2
        }
      ]
    }
  ]
}
```

## Example Responses

### Example 1: delete rules-batch
**Status:** `200 OK`

**Body:**
```javascript
{
  "tasks": [
    {
      "task-name": "delete-rules-batch",
      "task-id": "abcdef01-2345-6789-b8b5-8421f09bcf82",
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
