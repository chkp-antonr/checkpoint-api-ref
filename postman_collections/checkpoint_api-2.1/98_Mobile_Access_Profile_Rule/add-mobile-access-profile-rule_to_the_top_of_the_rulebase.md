# add-mobile-access-profile-rule to the top of the rulebase

**Collection:** Web API (version 2.1) > 98 Mobile Access Profile Rule
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-mobile-access-profile-rule`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "position": "top",
  "name": "Top Rule"
}
```

## Example Responses

### Example 1: add-mobile-access-profile-rule to the top of the rulebase
**Status:** `200 OK`
