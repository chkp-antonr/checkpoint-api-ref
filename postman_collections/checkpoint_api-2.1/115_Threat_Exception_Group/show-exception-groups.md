# show-exception-groups

**Collection:** Web API (version 2.1) > 115 Threat Exception Group
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-exception-groups`

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

### Example 1: show-exception-groups
**Status:** `200 OK`
