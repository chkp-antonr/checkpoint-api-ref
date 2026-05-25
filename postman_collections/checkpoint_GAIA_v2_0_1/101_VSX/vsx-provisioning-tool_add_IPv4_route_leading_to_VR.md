# vsx-provisioning-tool add IPv4 route leading to VR

**Collection:** Web API (version 2.0.1) > 101 VSX
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/vsx-provisioning-tool`

## Description

Add a new IPv4 route leading to a Virtual Router

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
    "destination": "10.1.1.0/24",
    "leads-to": "VR",
    "vd": "VS1"
  }
}
```

## Example Responses

### Example 1: vsx-provisioning-tool add IPv4 route leading to VR
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-abcd-1234-58dc02112100"
}
```
