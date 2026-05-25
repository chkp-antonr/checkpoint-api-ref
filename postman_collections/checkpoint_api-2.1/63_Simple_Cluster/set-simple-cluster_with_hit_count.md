# set-simple-cluster with hit count

**Collection:** Web API (version 2.1) > 63 Simple Cluster
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-simple-cluster`

## Description

Set simple cluster with hit count

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
  "hit-count": true
}
```

## Example Responses

### Example 1: set-simple-cluster with hit count
**Status:** `200 OK`
