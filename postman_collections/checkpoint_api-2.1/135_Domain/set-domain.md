# set-domain

**Collection:** Web API (version 2.1) > 135 Domain
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-domain`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "domain1",
  "comments": "This is domain1 comment"
}
```

## Example Responses

### Example 1: set-domain
**Status:** `200 OK`
