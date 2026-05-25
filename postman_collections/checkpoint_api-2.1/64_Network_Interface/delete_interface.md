# delete interface

**Collection:** Web API (version 2.1) > 64 Network Interface
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-interface`

## Description

Delete network interface.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "uid": "b7a5cb6f-1ad3-4193-b1ea-dda41308f79c"
}
```

## Example Responses

### Example 1: delete interface
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
