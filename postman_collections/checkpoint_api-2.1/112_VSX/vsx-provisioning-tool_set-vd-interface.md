# vsx-provisioning-tool set-vd-interface

**Collection:** Web API (version 2.1) > 112 VSX
**Method:** `POST`
**URL:** `{{server}}/v2.1/vsx-provisioning-tool`

## Description

Change the configuration of an interface on a Virtual Device

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "operation": "set-vd-interface",
  "set-vd-interface-params": {
    "name": "eth3",
    "anti-spoofing": "detect",
    "vd": "VS1",
    "anti-spoofing-tracking": "alert",
    "mtu": "1350"
  }
}
```

## Example Responses

### Example 1: vsx-provisioning-tool set-vd-interface
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-abcd-1234-58dc02112100"
}
```
