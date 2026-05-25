# get-platform

**Collection:** Web API (version 2.0.1) > 54 Gateways & Clusters
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/reset-sic`

## Description

Get platform from a gateway. Gateway supposed to be communicating to get platform successfully.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "gw1"
}
```

## Example Responses

### Example 1: get-platform
**Status:** `200 OK`

**Body:**
```javascript
{
  "tasks": [
    {
      "task-name": "get-platform",
      "task-id": "01234567-89ab-1234-9e1f-0e1e68312345",
      "status": "succeeded",
      "progress-percentage": 100,
      "suppressed": false,
      "task-details": [
        {
          "os-name": "Gaia",
          "version": "R81.10",
          "hardware": "Open Server"
        }
      ]
    }
  ]
}
```
