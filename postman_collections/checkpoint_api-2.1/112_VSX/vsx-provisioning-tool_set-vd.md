# vsx-provisioning-tool set-vd

**Collection:** Web API (version 2.1) > 112 VSX
**Method:** `POST`
**URL:** `{{server}}/v2.1/vsx-provisioning-tool`

## Description

Change the configuration of an existing Virtual System

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "operation": "set-vd",
  "set-vd-params": {
    "ipv4-instances": "3",
    "ipv6-instances": "2",
    "vd": "VS1"
  }
}
```

## Example Responses

### Example 1: vsx-provisioning-tool set-vd
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-abcd-1234-58dc02112100"
}
```
