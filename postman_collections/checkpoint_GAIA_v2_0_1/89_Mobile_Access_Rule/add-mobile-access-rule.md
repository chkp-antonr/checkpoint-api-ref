# add-mobile-access-rule

**Collection:** Web API (version 2.0.1) > 89 Mobile Access Rule
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-mobile-access-rule`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "position": 1,
  "name": "Rule 1",
  "applications": "New Application",
  "user-groups": [
    "my_group"
  ]
}
```

## Example Responses

### Example 1: add-mobile-access-rule
**Status:** `200 OK`
