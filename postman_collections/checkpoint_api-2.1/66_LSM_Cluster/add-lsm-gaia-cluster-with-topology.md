# add-lsm-gaia-cluster-with-topology

**Collection:** Web API (version 2.1) > 66 LSM Cluster
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-lsm-cluster`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name-prefix": "Gaia_",
  "main-ip-address": "192.168.8.197",
  "security-profile": "gaia_cluster",
  "topology": {
    "vpn-domain": "manual",
    "manual-vpn-domain": [
      {
        "from-ipv4-address": "1.1.1.1",
        "to-ipv4-address": "2.2.2.2",
        "comments": "range 1"
      },
      {
        "from-ipv4-address": "10.10.10.10",
        "to-ipv4-address": "10.10.10.20",
        "comments": "range 2"
      }
    ]
  },
  "interfaces": [
    {
      "name": "eth0",
      "new-name": "WAN",
      "member-network-override": "192.168.8.0",
      "ip-address-override": "192.168.8.197"
    },
    {
      "name": "eth1",
      "new-name": "LAN1",
      "member-network-override": "10.8.197.0",
      "ip-address-override": "10.8.197.1"
    },
    {
      "name": "eth2",
      "member-network-override": "10.10.10.0"
    }
  ],
  "members": [
    {
      "name": "Gaia_gw1",
      "sic": {
        "ip-address": "192.168.8.200",
        "one-time-password": "aaaa"
      }
    },
    {
      "name": "Gaia_gw2",
      "sic": {
        "ip-address": "192.168.8.202",
        "one-time-password": "aaaa"
      }
    }
  ]
}
```

## Example Responses

### Example 1: add-lsm-gaia-cluster-with-topology
**Status:** `200 OK`
