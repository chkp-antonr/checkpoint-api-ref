# delete tacacs-server

**Collection:** Web API (version 2.0.1) > 24 TACACS Server
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/delete-tacacs-server`

## Description

Delete an existing tacacs server

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "tacacs server"
}
```

## Example Responses

### Example 1: delete tacacs-server
**Status:** `200 OK`
