# add rules-batch

**Collection:** Web API (version 2.0.1) > 167 Rules Batch
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-rules-batch`

## Description

Add two access rules, two nat rules and two https rules

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
      "first-position": "top",
      "list": [
        {
          "name": "access rule 1",
          "action": "accept"
        },
        {
          "name": "access rule 2",
          "action": "accept"
        }
      ]
    },
    {
      "type": "nat-rule",
      "layer": "Standard",
      "first-position": "top",
      "list": [
        {
          "name": "nat rule 1"
        },
        {
          "name": "nat rule 2"
        }
      ]
    },
    {
      "type": "https-rule",
      "layer": "Default Layer",
      "first-position": "top",
      "list": [
        {
          "name": "https rule 1"
        },
        {
          "name": "https rule 2"
        }
      ]
    }
  ]
}
```

## Example Responses

### Example 1: add rules-batch
**Status:** `200 OK`

**Body:**
```javascript
{
  "tasks": [
    {
      "task-name": "add-rules-batch",
      "task-id": "abcdef01-2345-6789-b3e1-ec3bf46e699a",
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
