# show-application-sites

**Collection:** Web API (version 2.1) > 86 Application
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-application-sites`

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

### Example 1: show-application-sites
**Status:** `200 OK`
