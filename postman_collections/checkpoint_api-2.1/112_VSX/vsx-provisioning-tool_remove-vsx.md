# vsx-provisioning-tool remove-vsx

**Collection:** Web API (version 2.1) > 112 VSX
**Method:** `POST`
**URL:** `{{server}}/v2.1/vsx-provisioning-tool`

## Description

Remove a VSX Gateway

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "operation": "remove-vsx",
  "remove-vsx-params": {
    "vsx-name": "VSX_GATEWAY"
  }
}
```

## Example Responses

### Example 1: vsx-provisioning-tool remove-vsx
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-abcd-1234-58dc02112100"
}
```
