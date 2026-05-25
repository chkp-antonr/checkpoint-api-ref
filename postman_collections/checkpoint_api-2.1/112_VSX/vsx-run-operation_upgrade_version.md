# vsx-run-operation upgrade version

**Collection:** Web API (version 2.1) > 112 VSX
**Method:** `POST`
**URL:** `{{server}}/v2.1/vsx-run-operation`

## Description

Upgrade the version for a VSX Gateway or VSX Cluster object

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "operation": "upgrade",
  "upgrade-params": {
    "target-version": "R80.40",
    "vsx-name": "VSX_GW"
  }
}
```

## Example Responses

### Example 1: vsx-run-operation upgrade version
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-abcd-1234-58dc02112100"
}
```
