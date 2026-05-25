# add interface to cluster

**Collection:** Web API (version 2.0.1) > 57 Network Interface
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-interface`

## Description

Add network interface to cluster with two members.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "gateway-uid": "20ec49e8-8cd8-4ad4-b204-0de8ae4e0e17",
  "ipv4-address": "1.1.1.111",
  "ipv4-mask-length": 24,
  "name": "eth0",
  "anti-spoofing-settings": {
    "action": "detect",
    "exclude-packets": false,
    "spoof-tracking": "log"
  },
  "security-zone-settings": {
    "auto-calculated": false,
    "specific-zone": "InternalZone",
    "auto-calculated-zone": "InternalZone",
    "specific-security-zone-enabled": true
  },
  "topology-settings": {
    "interface-leads-to-dmz": false,
    "ip-address-behind-this-interface": "network defined by routing"
  },
  "topology": "internal",
  "cluster-network-type": "cluster",
  "cluster-members": [
    {
      "name": "eth4",
      "member-name": "member1",
      "member-uid": "5cba00d6-fb5f-42f6-b53e-ad0ce0391398",
      "ipv4-address": "2.2.2.1",
      "ipv4-network-mask": "255.255.255.0",
      "ipv4-mask-length": 24
    },
    {
      "name": "eth4",
      "member-name": "member2",
      "member-uid": "a02c65d7-a224-4dd5-8f5b-873ee7660aef",
      "ipv4-address": "2.2.2.2",
      "ipv4-network-mask": "255.255.255.0",
      "ipv4-mask-length": 24
    }
  ],
  "anti-spoofing": true,
  "ignore-warnings": false
}
```

## Example Responses

### Example 1: add interface to cluster
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "23865dbe-5a58-4902-abcb-36e894ad6f54",
  "name": "eth0",
  "type": "interface",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "topology-settings-automatic": {
    "ip-address-behind-this-interface": "not defined",
    "interface-leads-to-dmz": false
  },
  "topology-automatic": "internal",
  "topology-manual": "internal",
  "topology-settings-manual": {
    "ip-address-behind-this-interface": "network defined by routing",
    "interface-leads-to-dmz": false
  },
  "anti-spoofing-settings": {
    "action": "detect",
    "exclude-packets": false,
    "spoof-tracking": "log"
  },
  "network-interface-type": "ethernet",
  "security-zone-settings": {
    "auto-calculated-zone": "InternalZone",
    "auto-calculated-zone-uid": "e8131db2-8388-42a5-924a-82de32db20f7",
    "specific-zone-uid": "e8131db2-8388-42a5-924a-82de32db20f7",
    "specific-security-zone-enabled": true,
    "auto-calculated": false,
    "specific-zone": "InternalZone"
  },
  "cluster-members": [
    {
      "uid": "5e08c7a4-9686-49fb-a911-450099a07def",
      "name": "eth4",
      "member-uid": "5cba00d6-fb5f-42f6-b53e-ad0ce0391398",
      "member-name": "member1",
      "ipv4-address": "2.2.2.1",
      "ipv4-network-mask": "255.255.255.0",
      "ipv4-mask-length": 24,
      "ipv6-address": ""
    },
    {
      "uid": "38358bbe-f165-46ae-ae9a-3677a4c0d2d8",
      "name": "eth4",
      "member-uid": "a02c65d7-a224-4dd5-8f5b-873ee7660aef",
      "member-name": "member2",
      "ipv4-address": "2.2.2.2",
      "ipv4-network-mask": "255.255.255.0",
      "ipv4-mask-length": 24,
      "ipv6-address": ""
    }
  ],
  "anti-spoofing": true,
  "ipv4-address": "1.1.1.111",
  "ipv4-mask-length": 24,
  "cluster-network-type": "cluster",
  "gateway": {
    "type": "simple-cluster",
    "name": "dummy-cluster-1",
    "uid": "20ec49e8-8cd8-4ad4-b204-0de8ae4e0e17"
  },
  "comments": "",
  "color": "black",
  "tags": [],
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1685343309622,
      "iso-8601": "2023-05-29T09:55+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1685343308962,
      "iso-8601": "2023-05-29T09:55+0300"
    },
    "creator": "aa"
  },
  "read-only": true,
  "available-actions": {}
}
```
