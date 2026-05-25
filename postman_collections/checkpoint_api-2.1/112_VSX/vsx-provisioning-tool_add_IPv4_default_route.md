# vsx-provisioning-tool add IPv4 default route

**Collection:** Web API (version 2.1) > 112 VSX
**Method:** `POST`
**URL:** `{{server}}/v2.1/vsx-provisioning-tool`

## Description

Add a new IPv4 default route

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "operation": "add-route",
  "add-route-params": {
    "destination": "default",
    "next-hop": "192.168.1.254",
    "vd": "VS1"
  }
}
```

## Example Responses

### Example 1: vsx-provisioning-tool add IPv4 default route
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-abcd-1234-58dc02112100"
}
```
