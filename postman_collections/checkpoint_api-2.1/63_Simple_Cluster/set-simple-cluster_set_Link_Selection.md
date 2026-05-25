# set-simple-cluster (set Link Selection)

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
  "name": "cluster",
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

### Example 1: set-simple-cluster (set Link Selection)
**Status:** `200 OK`
