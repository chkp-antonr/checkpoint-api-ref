# vsx-run-operation remove cluster member

**Collection:** Web API (version 2.0.1) > 101 VSX
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/vsx-run-operation`

## Description

Remove a cluster member from an existing VSX cluster

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "operation": "remove-member",
  "remove-member-params": {
    "member-name": "Mem3"
  }
}
```

## Example Responses

### Example 1: vsx-run-operation remove cluster member
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-abcd-1234-58dc02112100"
}
```
