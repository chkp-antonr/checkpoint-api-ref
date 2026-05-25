# vsx-run-operation reconfigure VSX cluster member

**Collection:** Web API (version 2.1) > 112 VSX
**Method:** `POST`
**URL:** `{{server}}/v2.1/vsx-run-operation`

## Description

Reconfigure a VSX cluster member after a clean install

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "operation": "reconf-member",
  "reconf-member-params": {
    "member-name": "Mem3",
    "one-time-password": "abcdef",
    "ipv4-corexl-number": "4"
  }
}
```

## Example Responses

### Example 1: vsx-run-operation reconfigure VSX cluster member
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-abcd-1234-58dc02112100"
}
```
