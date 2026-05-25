# delete if-map-server

**Collection:** Web API (version 2.1) > 44 IF-MAP Server
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-if-map-server`

## Description

Delete existing IF-MAP server.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "TestIdp"
}
```

## Example Responses

### Example 1: delete if-map-server
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
