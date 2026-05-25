# set-lsm-smb-cluster

**Collection:** Web API (version 2.1) > 66 LSM Cluster
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-lsm-cluster`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "smb_smb_cluster",
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
      "name": "smb_gw1",
      "sic": {
        "ip-address": "192.168.8.200",
        "one-time-password": "aaaa"
      },
      "provisioning-state": "using-profile",
      "provisioning-settings": {
        "provisioning-profile": "prv_profile"
      }
    },
    {
      "name": "smb_gw2",
      "sic": {
        "ip-address": "192.168.8.202",
        "one-time-password": "aaaa"
      },
      "provisioning-state": "using-profile",
      "provisioning-settings": {
        "provisioning-profile": "smb_prv_profile"
      }
    }
  ]
}
```

## Example Responses

### Example 1: set-lsm-smb-cluster
**Status:** `200 OK`
