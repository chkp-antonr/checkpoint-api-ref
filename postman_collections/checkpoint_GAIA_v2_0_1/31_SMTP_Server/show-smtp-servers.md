# show-smtp-servers

**Collection:** Web API (version 2.0.1) > 31 SMTP Server
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-smtp-servers`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "limit": 50,
  "offset": 0,
  "details-level": "standard"
}
```

## Example Responses

### Example 1: show-smtp-servers
**Status:** `200 OK`
