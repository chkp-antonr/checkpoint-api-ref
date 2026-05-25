# add-network-with-NAT-static

**Collection:** Web API (version 2.0.1) > 06 Network
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-network`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Network 3",
  "subnet": "192.0.2.0",
  "subnet-mask": "255.255.255.0",
  "nat-settings": {
    "auto-rule": true,
    "method": "static",
    "ip-address": "192.0.2.1",
    "install-on": "All"
  }
}
```

## Example Responses

### Example 1: add-network-with-NAT-static
**Status:** `200 OK`
