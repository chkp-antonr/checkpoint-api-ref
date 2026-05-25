# add-simple-gateway with fetch policy

**Collection:** Web API (version 2.1) > 62 Simple Gateway
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-simple-gateway`

## Description

Fetch is done according to the order of the list

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
  "ipv4-address": "192.0.2.230",
  "fetch-policy": {
    "add": [
      "managementPri",
      "managementSec"
    ]
  }
}
```

## Example Responses

### Example 1: add-simple-gateway with fetch policy
**Status:** `200 OK`
