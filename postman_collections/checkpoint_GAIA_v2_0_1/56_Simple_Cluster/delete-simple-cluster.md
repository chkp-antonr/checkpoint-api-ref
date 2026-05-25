# delete-simple-cluster

**Collection:** Web API (version 2.0.1) > 56 Simple Cluster
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/delete-simple-cluster`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "cluster1"
}
```

## Example Responses

### Example 1: delete-simple-cluster
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
