# set-simple-cluster with exported routes: custom

**Collection:** Web API (version 2.1) > 63 Simple Cluster
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-simple-cluster`

## Description

Sets a simple cluster with custom exported routes

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
      "custom-routes": true,
      "custom-routes-object": "my_network"
    }
  }
}
```

## Example Responses

### Example 1: set-simple-cluster with exported routes: custom
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-cdef-94d9-ea3679371923"
}
```
