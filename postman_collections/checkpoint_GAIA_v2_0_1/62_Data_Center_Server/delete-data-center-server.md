# delete-data-center-server

**Collection:** Web API (version 2.0.1) > 62 Data Center Server
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/delete-data-center-server`

## Description

Delete an existing data center server.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "data-center-server-1"
}
```

## Example Responses

### Example 1: delete-data-center-server
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
