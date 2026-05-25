# set-simple-gateway with an addition to fetch policy

**Collection:** Web API (version 2.0.1) > 55 Simple Gateway
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-simple-gateway`

## Description

Fetch is done according to the order of the list, targets are always added at the end of the list

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
  "fetch-policy": {
    "add": [
      "managementSec"
    ]
  }
}
```

## Example Responses

### Example 1: set-simple-gateway with an addition to fetch policy
**Status:** `200 OK`
