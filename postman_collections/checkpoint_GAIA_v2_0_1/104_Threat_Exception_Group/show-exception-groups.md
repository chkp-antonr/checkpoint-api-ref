# show-exception-groups

**Collection:** Web API (version 2.0.1) > 104 Threat Exception Group
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-exception-groups`

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
