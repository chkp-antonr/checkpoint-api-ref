# set-global-properties with Network Location Awareness configurations

**Collection:** Web API (version 2.1) > 171 Global Properties
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-global-properties`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "remote-access": {
    "endpoint-connect": {
      "network-location-awareness": true,
      "network-location-awareness-conf": {
        "vpn-clients-are-considered-inside-the-internal-network-when-the-client": "connects from network or group",
        "network-or-group-of-conn-vpn-client": "someNetwork",
        "consider-wireless-networks-as-external": true,
        "excluded-internal-wireless-networks": {
          "add": "wirelessNetworkName"
        },
        "consider-undefined-dns-suffixes-as-external": true,
        "dns-suffixes": {
          "add": "aSuffix.com"
        }
      }
    }
  }
}
```

## Example Responses

### Example 1: set-global-properties with Network Location Awareness configurations
**Status:** `200 OK`
