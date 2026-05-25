# vsx-provisioning-tool remove-route

**Collection:** Web API (version 2.0.1) > 101 VSX
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/vsx-provisioning-tool`

## Description

Remove a route

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "operation": "remove-route",
  "remove-route-params": {
    "vd": "VS1",
    "destination": "192.168.1.0/24"
  }
}
```

## Example Responses

### Example 1: vsx-provisioning-tool remove-route
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-abcd-1234-58dc02112100"
}
```
