# vsx-provisioning-tool remove-physical-interface

**Collection:** Web API (version 2.1) > 112 VSX
**Method:** `POST`
**URL:** `{{server}}/v2.1/vsx-provisioning-tool`

## Description

Remove a physical interface from a VSX Gateway

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "operation": "remove-physical-interface",
  "remove-physical-interface-params": {
    "vsx-name": "VSX_GATEWAY",
    "name": "eth2"
  }
}
```

## Example Responses

### Example 1: vsx-provisioning-tool remove-physical-interface
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-abcd-1234-58dc02112100"
}
```
