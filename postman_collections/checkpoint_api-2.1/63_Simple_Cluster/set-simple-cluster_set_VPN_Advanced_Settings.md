# set-simple-cluster (set VPN Advanced Settings)

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
    "advanced": {
      "tunnel-sharing-mode": "custom-host-pair",
      "shutdown-on-gateway-restart": true,
      "enable-wire-mode": true,
      "wire-mode-interfaces": {
        "add": [
          "interface-1",
          "interface-2"
        ]
      },
      "enable-wire-mode-log-traffic": true,
      "enable-nat-traversal": true
    }
  }
}
```

## Example Responses

### Example 1: set-simple-cluster (set VPN Advanced Settings)
**Status:** `200 OK`
