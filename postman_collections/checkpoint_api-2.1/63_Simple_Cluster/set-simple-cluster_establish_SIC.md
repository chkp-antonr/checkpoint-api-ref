# set-simple-cluster establish SIC

**Collection:** Web API (version 2.1) > 63 Simple Cluster
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-simple-cluster`

## Description

Establish SIC with existing cluster members

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "cluster1",
  "members": {
    "update": [
      {
        "name": "member1",
        "one-time-password": "abcd"
      },
      {
        "name": "member2",
        "one-time-password": "abcd"
      }
    ]
  }
}
```

## Example Responses

### Example 1: set-simple-cluster establish SIC
**Status:** `200 OK`
