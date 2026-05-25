# add-simple-cluster

**Collection:** Web API (version 2.0.1) > 56 Simple Cluster
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-simple-cluster`

## Description

Add a simple cluster with two members and three interfaces

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "cluster1",
  "color": "yellow",
  "version": "R80.30",
  "ip-address": "17.23.5.1",
  "os-name": "Gaia",
  "cluster-mode": "cluster-xl-ha",
  "firewall": true,
  "vpn": false,
  "interfaces": [
    {
      "name": "eth0",
      "ip-address": "17.23.5.1",
      "network-mask": "255.255.255.0",
      "interface-type": "cluster",
      "topology": "EXTERNAL",
      "anti-spoofing": true
    },
    {
      "name": "eth1",
      "interface-type": "sync",
      "topology": "INTERNAL",
      "topology-settings": {
        "ip-address-behind-this-interface": "network defined by the interface ip and net mask",
        "interface-leads-to-dmz": false
      }
    },
    {
      "name": "eth2",
      "ip-address": "192.168.1.1",
      "network-mask": "255.255.255.0",
      "interface-type": "cluster",
      "topology": "INTERNAL",
      "anti-spoofing": true,
      "topology-settings": {
        "ip-address-behind-this-interface": "network defined by the interface ip and net mask",
        "interface-leads-to-dmz": false
      }
    }
  ],
  "members": [
    {
      "name": "member1",
      "one-time-password": "abcd",
      "ip-address": "17.23.5.2",
      "interfaces": [
        {
          "name": "eth0",
          "ip-address": "17.23.5.2",
          "network-mask": "255.255.255.0"
        },
        {
          "name": "eth1",
          "ip-address": "1.1.2.4",
          "network-mask": "255.255.255.0"
        },
        {
          "name": "eth2",
          "ip-address": "192.168.1.2",
          "network-mask": "255.255.255.0"
        }
      ]
    },
    {
      "name": "member2",
      "one-time-password": "abcd",
      "ip-address": "17.23.5.3",
      "interfaces": [
        {
          "name": "eth0",
          "ip-address": "17.23.5.3",
          "network-mask": "255.255.255.0"
        },
        {
          "name": "eth1",
          "ip-address": "1.1.2.5",
          "network-mask": "255.255.255.0"
        },
        {
          "name": "eth2",
          "ip-address": "192.168.1.3",
          "network-mask": "255.255.255.0"
        }
      ]
    }
  ]
}
```

## Example Responses

### Example 1: add-simple-cluster
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-abcd-1234-58dc02112100"
}
```
