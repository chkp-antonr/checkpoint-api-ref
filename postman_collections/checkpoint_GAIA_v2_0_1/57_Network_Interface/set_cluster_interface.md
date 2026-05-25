# set cluster interface

**Collection:** Web API (version 2.0.1) > 57 Network Interface
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-interface`

## Description

Modify an existing cluster network interface, set internal topology as network defined by the interface ip and net mask and enable anti-spoofing.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "uid": "19453b2b-a676-4cfa-b75e-293af0ee3a6e",
  "ipv4-address": "1.1.2.11",
  "ipv4-mask-length": 24,
  "name": "eth1",
  "cluster-network-type": "cluster",
  "topology-settings": {
    "interface-leads-to-dmz": false,
    "ip-address-behind-this-interface": "network defined by the interface ip and net mask"
  },
  "topology": "internal",
  "cluster-members": [
    {
      "uid": "b101085b-84e1-4fdd-a677-1e0727627714",
      "ipv4-address": "1.1.2.3",
      "ipv4-mask-length": 24
    },
    {
      "uid": "ddaae797-592c-454a-8366-2088e0ba5b1d",
      "ipv4-address": "1.1.2.5",
      "ipv4-mask-length": 24
    }
  ],
  "anti-spoofing": true
}
```

## Example Responses

### Example 1: set cluster interface
**Status:** `200 OK`
