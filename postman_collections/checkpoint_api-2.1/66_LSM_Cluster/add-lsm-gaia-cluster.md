# add-lsm-gaia-cluster

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

### Example 1: add-lsm-gaia-cluster
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "d1c363bc-c4c6-4903-9426-495d800b47ae",
  "name": "Gaia_gaia_cluster",
  "type": "lsm-cluster",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1608633933685,
      "iso-8601": "2020-12-22T12:45+0200"
    },
    "last-modifier": "System",
    "creation-time": {
      "posix": 1608633909531,
      "iso-8601": "2020-12-22T12:45+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": false,
  "comments": "this object was created via API",
  "color": "black",
  "icon": "NetworkObjects/ROBO/ROBO_CLUSTER",
  "security-profile": "gaia_cluster",
  "main-ip-address": "192.168.68.197",
  "version": "R81.10",
  "os-name": "Gaia",
  "members": [
    {
      "member-uid": "6c015875-6776-4066-8735-9c4f43e3787d",
      "member-name": "Gaia_gw1",
      "sic-name": "CN=Gaia_gw1,O=R81.10_API..wm5cer",
      "sic-state": "Initialized",
      "main-ip-address": "192.168.8.200",
      "interfaces": [
        {
          "name": "WAN",
          "ip-address": "192.168.8.200"
        },
        {
          "name": "LAN1",
          "ip-address": "10.8.197.200"
        }
      ]
    },
    {
      "member-uid": "6e648bd7-c686-46db-a0f1-0d1d794f4ea9",
      "member-name": "Gaia_gw2",
      "sic-name": "CN=Gaia_gw2,O=R81.10_API_Cluster..wm5cer",
      "sic-state": "Initialized",
      "main-ip-address": "192.168.8.202",
      "interfaces": [
        {
          "name": "WAN",
          "ip-address": "192.168.8.202"
        },
        {
          "name": "LAN1",
          "ip-address": "10.8.197.202"
        }
      ]
    }
  ],
  "interfaces": [
    {
      "name": "WAN",
      "member-network-override": "192.168.68.0",
      "cluster-ip-address-override": "192.168.68.197"
    },
    {
      "name": "LAN1",
      "member-network-override": "10.8.197.0",
      "cluster-ip-address-override": "10.8.197.1"
    }
  ]
}
```
