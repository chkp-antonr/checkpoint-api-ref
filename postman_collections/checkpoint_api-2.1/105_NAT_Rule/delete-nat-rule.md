# delete-nat-rule

**Collection:** Web API (version 2.1) > 105 NAT Rule
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-nat-rule`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "rule-number": 1,
  "package": "standard"
}
```

## Example Responses

### Example 1: delete-nat-rule
**Status:** `200 OK`
