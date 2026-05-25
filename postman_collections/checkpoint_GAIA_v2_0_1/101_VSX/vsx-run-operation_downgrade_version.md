# vsx-run-operation downgrade version

**Collection:** Web API (version 2.0.1) > 101 VSX
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/vsx-run-operation`

## Description

Downgrade the version for VSX Gateway or VSX Cluster object

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "operation": "downgrade",
  "downgrade-params": {
    "target-version": "R80.40",
    "vsx-name": "VSX_CLUSTER"
  }
}
```

## Example Responses

### Example 1: vsx-run-operation downgrade version
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-abcd-1234-58dc02112100"
}
```
