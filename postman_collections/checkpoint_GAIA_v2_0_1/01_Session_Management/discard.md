# discard

**Collection:** Web API (version 2.0.1) > 01 Session Management
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/discard`

## Description

Discard the changes

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

### Example 1: discard
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK",
  "number-of-discarded-changes": 0
}
```
