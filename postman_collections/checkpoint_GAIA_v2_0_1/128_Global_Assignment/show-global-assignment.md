# show-global-assignment

**Collection:** Web API (version 2.0.1) > 128 Global Assignment
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-global-assignment`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "global-domain": "Global2",
  "dependent-domain": "domain1"
}
```

## Example Responses

### Example 1: show-global-assignment
**Status:** `200 OK`
