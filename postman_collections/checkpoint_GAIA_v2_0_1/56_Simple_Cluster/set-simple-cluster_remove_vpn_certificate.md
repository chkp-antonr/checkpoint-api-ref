# set-simple-cluster remove vpn certificate

**Collection:** Web API (version 2.0.1) > 56 Simple Cluster
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-simple-cluster`

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
  "vpn-settings": {
    "certificates": {
      "remove": "new_cert1"
    }
  },
  "ignore-warnings": "true"
}
```

## Example Responses

### Example 1: set-simple-cluster remove vpn certificate
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-cdef-94d9-ea3679371923"
}
```
