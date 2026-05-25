# set-simple-cluster with ips settings

**Collection:** Web API (version 2.1) > 63 Simple Cluster
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-simple-cluster`

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
  "ips": true,
  "ips-settings": {
    "bypass-all-under-load": false,
    "bypass-track-method": "log",
    "top-cpu-consuming-protections": {
      "disable-under-load": true,
      "disable-period": 8
    }
  }
}
```

## Example Responses

### Example 1: set-simple-cluster with ips settings
**Status:** `200 OK`
