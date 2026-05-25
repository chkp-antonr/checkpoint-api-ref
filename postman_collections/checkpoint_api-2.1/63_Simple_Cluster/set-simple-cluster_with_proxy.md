# set-simple-cluster with proxy

**Collection:** Web API (version 2.1) > 63 Simple Cluster
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-simple-cluster`

## Description

set simple cluster with proxy settings

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
  "proxy-settings": {
    "use-custom-proxy": true,
    "proxy-server": "checkpoint",
    "port": "8080"
  }
}
```

## Example Responses

### Example 1: set-simple-cluster with proxy
**Status:** `200 OK`
