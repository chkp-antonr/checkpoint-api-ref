# delete logical-server

**Collection:** Web API (version 2.1) > 24 Logical Server
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-logical-server`

## Description

Delete existing logical server.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "logicalServer1"
}
```

## Example Responses

### Example 1: delete logical-server
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
