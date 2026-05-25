# vsx-provisioning-tool add-vd

**Collection:** Web API (version 2.1) > 112 VSX
**Method:** `POST`
**URL:** `{{server}}/v2.1/vsx-provisioning-tool`

## Description

Add a new Virtual System to an existing VSX cluster

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "operation": "add-vd",
  "add-vd-params": {
    "vd": "NEW_VD",
    "vsx-name": "VSX_CLUSTER",
    "type": "vs",
    "ipv4-instances": "2",
    "ipv4-address": "192.168.1.1",
    "interfaces": {
      "1": {
        "name": "eth1",
        "ipv4-address": "192.168.1.1/24"
      }
    }
  }
}
```

## Example Responses

### Example 1: vsx-provisioning-tool add-vd
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-abcd-1234-58dc02112100"
}
```
