# set-smtp-server

**Collection:** Web API (version 2.0.1) > 31 SMTP Server
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-smtp-server`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "SMTP",
  "server": "smtp.example.com",
  "port": "25"
}
```

## Example Responses

### Example 1: set-smtp-server
**Status:** `200 OK`
