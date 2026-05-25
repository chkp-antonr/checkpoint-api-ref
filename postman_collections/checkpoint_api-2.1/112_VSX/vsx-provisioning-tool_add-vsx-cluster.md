# vsx-provisioning-tool add-vsx-cluster

**Collection:** Web API (version 2.1) > 112 VSX
**Method:** `POST`
**URL:** `{{server}}/v2.1/vsx-provisioning-tool`

## Description

Add a VSX cluster with 2 cluster members

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "operation": "add-vsx-cluster",
  "add-vsx-cluster-params": {
    "vsx-name": "VSX_CLUSTER",
    "cluster-type": "vsls",
    "version": "R81.10",
    "ipv4-address": "10.1.1.15",
    "sync-if-name": "eth3",
    "sync-netmask": "255.255.255.0",
    "rule-ping": "enable",
    "rule-drop": "enable",
    "members": [
      {
        "name": "VSX1",
        "ipv4-address": "10.1.1.1",
        "sync-ip": "192.168.1.1",
        "sic-otp": "sicotp123"
      },
      {
        "name": "VSX2",
        "ipv4-address": "10.1.1.2",
        "sync-ip": "192.168.1.2",
        "sic-otp": "sicotp123"
      }
    ]
  }
}
```

## Example Responses

### Example 1: vsx-provisioning-tool add-vsx-cluster
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-abcd-1234-58dc02112100"
}
```
