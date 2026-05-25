# show-lsm-cluster-profile

**Collection:** Web API (version 2.0.1) > 161 LSM Cluster Profile
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-lsm-cluster-profile`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "cluster_profile"
}
```

## Example Responses

### Example 1: show-lsm-cluster-profile
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "cbc1b062-73e3-4ee7-8eb1-2c833f540230",
  "name": "cluster_profile",
  "type": "lsm-cluster-profile",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "cluster-members": [
    {
      "uid": "5f06812f-c6b2-4f0b-9245-1b6565d00857",
      "name": "m1",
      "ip-address": "192.168.68.56",
      "comments": ""
    },
    {
      "uid": "ea9cfc85-6e1f-47dd-88fb-3bbe5bbd9aee",
      "name": "m2",
      "ip-address": "192.168.68.57",
      "comments": ""
    }
  ],
  "cluster-interfaces": [
    {
      "name": "eth0",
      "network-address": "192.168.68.0",
      "network-mask": "255.255.255.0",
      "topology": {
        "type": "external",
        "ip-addresses-behind-this-interface": "not-defined",
        "anti-spoofing": true,
        "anti-spoofing-settings": {
          "action": "detect",
          "do-not-check-specific-packets": false,
          "do-not-check-specific-packets-from": "",
          "spoof-tracking": "log"
        },
        "interface-leads-to-dmz": false
      }
    },
    {
      "name": "eth1",
      "network-address": "10.68.68.0",
      "network-mask": "255.255.255.0",
      "topology": {
        "type": "internal",
        "anti-spoofing": true,
        "anti-spoofing-settings": {
          "action": "detect",
          "do-not-check-specific-packets": false,
          "do-not-check-specific-packets-from": "",
          "spoof-tracking": "log"
        },
        "interface-leads-to-dmz": false
      }
    }
  ],
  "dynamic-ip": false,
  "version": "R81",
  "firewall": true,
  "vpn": false,
  "application-control": false,
  "url-filtering": false,
  "threat-prevention-mode": "custom",
  "ips": false,
  "threat-emulation": false,
  "threat-extraction": false,
  "anti-bot": false,
  "anti-virus": false,
  "content-awareness": false,
  "save-logs-locally": false,
  "send-alerts-to-server": [],
  "send-logs-to-server": [],
  "send-logs-to-backup-server": [],
  "identity-awareness": false,
  "groups": [
    {
      "uid": "68a56016-ac11-4c9b-b584-976162b15d1d",
      "name": "Gaia_Cluster",
      "type": "lsm-cluster",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "NetworkObjects/ROBO/ROBO_CLUSTER",
      "color": "black"
    }
  ],
  "comments": "",
  "color": "black",
  "icon": "Profiles/lsm_profile",
  "tags": [],
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1629896065414,
      "iso-8601": "2021-08-25T15:54+0300"
    },
    "last-modifier": "bb",
    "creation-time": {
      "posix": 1629791483018,
      "iso-8601": "2021-08-24T10:51+0300"
    },
    "creator": "aa"
  },
  "read-only": false
}
```
