# vsx-provisioning-tool add-vd-interface

**Collection:** Web API (version 2.1) > 112 VSX
**Method:** `POST`
**URL:** `{{server}}/v2.1/vsx-provisioning-tool`

## Description

Add a new interface to a Virtual System

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "operation": "add-vd-interface",
  "add-vd-interface-params": {
    "name": "eth3",
    "ipv4-address": "192.168.1.1/24",
    "vd": "VS1"
  }
}
```

## Example Responses

### Example 1: vsx-provisioning-tool add-vd-interface
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-abcd-1234-58dc02112100"
}
```
