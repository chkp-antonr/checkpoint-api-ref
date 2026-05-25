# keepalive

**Collection:** Web API (version 2.0.1) > 01 Session Management
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/keepalive`

## Description

Keep the session alive

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{}
```

## Example Responses

### Example 1: keepalive
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
