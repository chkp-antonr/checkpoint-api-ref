# show-repository-scripts

**Collection:** Web API (version 2.1) > 145 Repository Scripts
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-repository-scripts`

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

### Example 1: show-repository-scripts
**Status:** `200 OK`
