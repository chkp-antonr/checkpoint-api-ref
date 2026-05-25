# vsx-run-operation add cluster member

**Collection:** Web API (version 2.0.1) > 101 VSX
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/vsx-run-operation`

## Description

Add a new member to an existing VSX cluster

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "operation": "add-member",
  "add-member-params": {
    "vsx-name": "VSX_CLUSTER",
    "member-name": "Mem3",
    "ipv4-address": "25.25.25.223",
    "ipv4-sync-address": "20.20.20.223"
  }
}
```

## Example Responses

### Example 1: vsx-run-operation add cluster member
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-abcd-1234-58dc02112100"
}
```
