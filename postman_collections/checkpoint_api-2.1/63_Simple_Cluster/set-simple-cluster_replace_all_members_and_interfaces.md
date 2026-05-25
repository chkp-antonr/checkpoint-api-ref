# set-simple-cluster replace all members and interfaces

**Collection:** Web API (version 2.1) > 63 Simple Cluster
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-simple-cluster`

## Description

Replace all cluster members and all interfaces

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
      "name": "eth-0",
      "ip-address": "17.2.9.1",
      "network-mask": "255.255.255.0",
      "interface-type": "cluster",
      "topology": "EXTERNAL",
      "anti-spoofing": true
    },
    {
      "name": "eth-1",
      "interface-type": "sync",
      "topology": "INTERNAL"
    },
    {
      "name": "eth-2",
      "ip-address": "192.168.99.1",
      "network-mask": "255.255.255.0",
      "interface-type": "cluster",
      "topology": "INTERNAL",
      "anti-spoofing": true
    }
  ],
  "members": [
    {
      "name": "mem-1",
      "one-time-password": "aaaa",
      "ip-address": "17.2.6.9",
      "interfaces": [
        {
          "name": "eth-0",
          "ip-address": "17.2.6.10",
          "network-mask": "255.255.255.0"
        },
        {
          "name": "eth-1",
          "ip-address": "1.1.99.4",
          "network-mask": "255.255.255.0"
        },
        {
          "name": "eth-2",
          "ip-address": "192.168.99.2",
          "network-mask": "255.255.255.0"
        }
      ]
    },
    {
      "name": "mem-2",
      "one-time-password": "aaaa",
      "ip-address": "17.2.6.8",
      "interfaces": [
        {
          "name": "eth-0",
          "ip-address": "17.2.6.49",
          "network-mask": "255.255.255.0"
        },
        {
          "name": "eth-1",
          "ip-address": "1.1.99.5",
          "network-mask": "255.255.255.0"
        },
        {
          "name": "eth-2",
          "ip-address": "192.168.99.3",
          "network-mask": "255.255.255.0"
        }
      ]
    }
  ]
}
```

## Example Responses

### Example 1: set-simple-cluster replace all members and interfaces
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-abcd-1234-58dc02112100"
}
```
