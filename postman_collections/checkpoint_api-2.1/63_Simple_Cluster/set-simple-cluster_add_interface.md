# set-simple-cluster add interface

**Collection:** Web API (version 2.1) > 63 Simple Cluster
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-simple-cluster`

## Description

Add interface to cluster and all members

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
  "interfaces": {
    "add": {
      "name": "eth3",
      "ip-address": "10.10.10.1",
      "ipv4-mask-length": "24",
      "interface-type": "cluster",
      "topology": "INTERNAL",
      "anti-spoofing": "true"
    }
  },
  "members": {
    "update": [
      {
        "name": "member1",
        "interfaces": {
          "name": "eth3",
          "ipv4-address": "10.10.10.2",
          "ipv4-network-mask": "255.255.255.0"
        }
      },
      {
        "name": "member2",
        "interfaces": {
          "name": "eth3",
          "ipv4-address": "10.10.10.3",
          "ipv4-network-mask": "255.255.255.0"
        }
      }
    ]
  }
}
```

## Example Responses

### Example 1: set-simple-cluster add interface
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-abcd-1234-58dc02112100"
}
```
