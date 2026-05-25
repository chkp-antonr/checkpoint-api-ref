# set-simple-gateway with change of order to fetch policy list 

**Collection:** Web API (version 2.1) > 62 Simple Gateway
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-simple-gateway`

## Description

All list must be overridden

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "gw1",
  "fetch-policy": [
    "managementSec",
    "managementPri"
  ]
}
```

## Example Responses

### Example 1: set-simple-gateway with change of order to fetch policy list 
**Status:** `200 OK`
