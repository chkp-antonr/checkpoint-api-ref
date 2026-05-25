# vsx-run-operation reconfigure VSX GW

**Collection:** Web API (version 2.0.1) > 101 VSX
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/vsx-run-operation`

## Description

Reconfigure a VSX Gateway after a clean install

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "operation": "reconf-gw",
  "reconf-gw-params": {
    "vsx-name": "VSX_GW",
    "one-time-password": "abcdef",
    "ipv4-corexl-number": "4"
  }
}
```

## Example Responses

### Example 1: vsx-run-operation reconfigure VSX GW
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-abcd-1234-58dc02112100"
}
```
