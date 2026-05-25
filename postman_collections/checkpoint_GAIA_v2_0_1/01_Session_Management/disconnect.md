# disconnect

**Collection:** Web API (version 2.0.1) > 01 Session Management
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/disconnect`

## Description

Disconnect a private session

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde"
}
```

## Example Responses

### Example 1: disconnect
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
