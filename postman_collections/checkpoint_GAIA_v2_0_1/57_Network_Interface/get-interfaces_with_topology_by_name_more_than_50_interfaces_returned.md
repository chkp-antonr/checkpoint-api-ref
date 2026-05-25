# get-interfaces with topology by name, more than 50 interfaces returned

**Collection:** Web API (version 2.0.1) > 57 Network Interface
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/get-interfaces`

## Description

Get physical interfaces with or without their topology from a Gaia Security Gateway or Cluster that is specified by its object name and contains more than 50 interfaces. Note: The response contains only the first 50 interfaces and the total number of interfaces in the object.

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

### Example 1: get-interfaces with topology by name, more than 50 interfaces returned
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
            "eth1",
            "...",
            "eth49"
          ],
          "total": 85
        }
      ]
    }
  ]
}
```
