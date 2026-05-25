# add-simple-cluster with exported routes

**Collection:** Web API (version 2.1) > 63 Simple Cluster
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-simple-cluster`

## Description

Adds a simple cluster with custom exported routes

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
  "vpn-settings": {
    "exported-routes": {
      "custom-routes": true,
      "custom-routes-object": "my_network"
    }
  },
  "ip-address": "17.23.5.1",
  "vpn": true,
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

### Example 1: add-simple-cluster with exported routes
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-abcd-1234-58dc02112100"
}
```
