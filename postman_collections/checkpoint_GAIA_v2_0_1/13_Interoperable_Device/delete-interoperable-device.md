# delete-interoperable-device

**Collection:** Web API (version 2.0.1) > 13 Interoperable Device
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/delete-interoperable-device`

## Description

Deletes a simple Interoperable Device

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "NewInteroperableDevice"
}
```

## Example Responses

### Example 1: delete-interoperable-device
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
