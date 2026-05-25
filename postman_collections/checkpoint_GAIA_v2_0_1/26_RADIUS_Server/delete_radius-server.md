# delete radius-server

**Collection:** Web API (version 2.0.1) > 26 RADIUS Server
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/delete-radius-server`

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
