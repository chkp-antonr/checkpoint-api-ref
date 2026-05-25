# add-simple-gateway with sic

**Collection:** Web API (version 2.0.1) > 55 Simple Gateway
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-simple-gateway`

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
  "color": "yellow",
  "ipv4-address": "192.0.2.230",
  "version": "R80",
  "one-time-password": "aaaa",
  "firewall": true,
  "vpn": true,
  "application-control": true,
  "url-filtering": true,
  "ips": true,
  "anti-bot": true,
  "anti-virus": true,
  "threat-emulation": true,
  "nat-hide-internal-interfaces": true,
  "icap-server": true,
  "interfaces": [
    {
      "name": "eth0",
      "ipv4-address": "192.0.2.230",
      "ipv4-network-mask": "255.255.255.128",
      "anti-spoofing": true,
      "topology": "EXTERNAL"
    },
    {
      "name": "eth1",
      "ipv4-address": "192.0.2.88",
      "ipv4-network-mask": "255.255.255.0",
      "anti-spoofing": true,
      "topology": "INTERNAL"
    }
  ]
}
```

## Example Responses

### Example 1: add-simple-gateway with sic
**Status:** `200 OK`
