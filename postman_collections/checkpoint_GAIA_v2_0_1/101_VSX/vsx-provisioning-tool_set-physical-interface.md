# vsx-provisioning-tool set-physical-interface

**Collection:** Web API (version 2.0.1) > 101 VSX
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/vsx-provisioning-tool`

## Description

Change the configuration of a physical interface

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "operation": "set-physical-interface",
  "set-physical-interface-params": {
    "name": "eth3",
    "vlan-trunk": "true",
    "vsx-name": "VSX-GW"
  }
}
```

## Example Responses

### Example 1: vsx-provisioning-tool set-physical-interface
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-abcd-1234-58dc02112100"
}
```
