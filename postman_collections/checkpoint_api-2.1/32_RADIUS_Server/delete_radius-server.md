# delete radius-server

**Collection:** Web API (version 2.1) > 32 RADIUS Server
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-radius-server`

## Description

Delete an existing radius server

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "radiusServer",
  "ignore-warnings": "true"
}
```

## Example Responses

### Example 1: delete radius-server
**Status:** `200 OK`
