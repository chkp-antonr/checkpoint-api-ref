# set-simple-cluster with fetch policy

**Collection:** Web API (version 2.0.1) > 56 Simple Cluster
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-simple-cluster`

## Description

Set simple cluster with fetch policy

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
  "fetch-policy": {
    "add": [
      "managementObj1",
      "managementObj2"
    ]
  }
}
```

## Example Responses

### Example 1: set-simple-cluster with fetch policy
**Status:** `200 OK`
