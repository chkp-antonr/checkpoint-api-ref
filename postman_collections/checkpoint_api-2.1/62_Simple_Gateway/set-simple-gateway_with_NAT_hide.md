# set-simple-gateway with NAT hide

**Collection:** Web API (version 2.1) > 62 Simple Gateway
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-simple-gateway`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "gw1",
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

### Example 1: set-simple-gateway with NAT hide
**Status:** `200 OK`
