# set-simple-cluster scale up

**Collection:** Web API (version 2.0.1) > 56 Simple Cluster
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-simple-cluster`

## Description

Scale up simple cluster with an additional member

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
  "members": {
    "add": {
      "name": "member3",
      "ipv4-address": "17.23.5.4",
      "one-time-password": "aaaa",
      "interfaces": [
        {
          "name": "eth0",
          "ip-address": "17.23.5.4",
          "network-mask": "255.255.255.0"
        },
        {
          "name": "eth1",
          "ip-address": "1.1.2.6",
          "network-mask": "255.255.255.0"
        },
        {
          "name": "eth2",
          "ip-address": "192.168.1.4",
          "network-mask": "255.255.255.0"
        }
      ]
    }
  }
}
```

## Example Responses

### Example 1: set-simple-cluster scale up
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-abcd-1234-58dc02112100"
}
```
