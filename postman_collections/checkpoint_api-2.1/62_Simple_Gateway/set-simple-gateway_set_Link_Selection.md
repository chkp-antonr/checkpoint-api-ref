# set-simple-gateway (set Link Selection)

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
  "name": "gw",
  "vpn-settings": {
    "link-selection": {
      "ip-selection": "use-selected-address-from-topology",
      "ip-address": "192.168.0.1",
      "route-selection-method": "os-routing-table",
      "responding-traffic": "use-outgoing-traffic-configuration",
      "source-ip-selection": "main",
      "outgoing-link-tracking": "log"
    }
  }
}
```

## Example Responses

### Example 1: set-simple-gateway (set Link Selection)
**Status:** `200 OK`
