# set-simple-cluster replace all interfaces

**Collection:** Web API (version 2.1) > 63 Simple Cluster
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-simple-cluster`

## Description

Replace all cluster and members interfaces with new interfaces

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
  "interfaces": [
    {
      "name": "eth0",
      "ip-address": "1.1.1.1",
      "network-mask": "255.255.255.0",
      "interface-type": "cluster",
      "topology": "EXTERNAL",
      "anti-spoofing": "false"
    },
    {
      "name": "eth1",
      "ip-address": "2.2.2.1",
      "network-mask": "255.255.255.0",
      "interface-type": "cluster",
      "topology": "INTERNAL",
      "anti-spoofing": "false"
    }
  ],
  "members": {
    "update": [
      {
        "name": "member1",
        "ip-address": "1.1.1.2",
        "interfaces": [
          {
            "name": "eth0",
            "ipv4-address": "1.1.1.2",
            "ipv4-network-mask": "255.255.255.0"
          },
          {
            "name": "eth1",
            "ipv4-address": "2.2.2.2",
            "ipv4-network-mask": "255.255.255.0"
          }
        ]
      },
      {
        "name": "member2",
        "ip-address": "1.1.1.3",
        "interfaces": [
          {
            "name": "eth0",
            "ipv4-address": "1.1.1.3",
            "ipv4-network-mask": "255.255.255.0"
          },
          {
            "name": "eth1",
            "ipv4-address": "2.2.2.3",
            "ipv4-network-mask": "255.255.255.0"
          }
        ]
      }
    ]
  }
}
```

## Example Responses

### Example 1: set-simple-cluster replace all interfaces
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-abcd-1234-58dc02112100"
}
```
