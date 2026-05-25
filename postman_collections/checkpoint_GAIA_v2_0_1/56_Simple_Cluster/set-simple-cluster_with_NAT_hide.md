# set-simple-cluster with NAT hide

**Collection:** Web API (version 2.0.1) > 56 Simple Cluster
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-simple-cluster`

## Description

Set simple cluster with NAT

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
  "nat-hide-internal-interfaces": true,
  "nat-settings": {
    "auto-rule": true,
    "method": "hide",
    "hide-behind": "ip-address",
    "ipv4-address": "192.0.2.1",
    "install-on": "All"
  }
}
```

## Example Responses

### Example 1: set-simple-cluster with NAT hide
**Status:** `200 OK`
