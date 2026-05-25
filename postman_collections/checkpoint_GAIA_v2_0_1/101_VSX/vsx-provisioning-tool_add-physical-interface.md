# vsx-provisioning-tool add-physical-interface

**Collection:** Web API (version 2.0.1) > 101 VSX
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/vsx-provisioning-tool`

## Description

Add a new physical interface to a VSX Gateway

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "operation": "add-physical-interface",
  "add-physical-interface-params": {
    "name": "eth3",
    "vlan-trunk": "false",
    "vsx-name": "VSX-GW"
  }
}
```

## Example Responses

### Example 1: vsx-provisioning-tool add-physical-interface
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-abcd-1234-58dc02112100"
}
```
