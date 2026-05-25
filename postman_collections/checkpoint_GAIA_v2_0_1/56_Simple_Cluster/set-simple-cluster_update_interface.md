# set-simple-cluster update interface

**Collection:** Web API (version 2.0.1) > 56 Simple Cluster
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-simple-cluster`

## Description

Update an existing cluster interface. Change any of the interface settings except for the interface name

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
    "update": {
      "name": "eth-1",
      "ip-address": "1.2.2.203",
      "network-mask": "255.255.255.0",
      "interface-type": "cluster",
      "topology": "INTERNAL",
      "topology-settings": {
        "ip-address-behind-this-interface": "network defined by the interface ip and net mask",
        "interface-leads-to-dmz": false
      }
    }
  }
}
```

## Example Responses

### Example 1: set-simple-cluster update interface
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-abcd-1234-58dc02112100"
}
```
