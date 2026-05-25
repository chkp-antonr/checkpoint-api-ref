# set-simple-cluster with exported routes: internal interfaces

**Collection:** Web API (version 2.1) > 63 Simple Cluster
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-simple-cluster`

## Description

Sets a simple cluster with exported routes mode internal interfaces

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
    "exported-routes": {
      "internal-interfaces": true
    }
  }
}
```

## Example Responses

### Example 1: set-simple-cluster with exported routes: internal interfaces
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-cdef-94d9-ea3679371923"
}
```
