# vsx-provisioning-tool attach-bridge

**Collection:** Web API (version 2.0.1) > 101 VSX
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/vsx-provisioning-tool`

## Description

Attach a bridge interface to an existing Virtual System

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "operation": "attach-bridge",
  "attach-bridge-params": {
    "vd": "VS1",
    "ifs1": "eth6",
    "ifs2": "eth7"
  }
}
```

## Example Responses

### Example 1: vsx-provisioning-tool attach-bridge
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-abcd-1234-58dc02112100"
}
```
