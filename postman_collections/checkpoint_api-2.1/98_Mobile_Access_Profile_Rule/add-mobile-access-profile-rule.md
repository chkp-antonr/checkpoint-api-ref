# add-mobile-access-profile-rule

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
  "position": 1,
  "name": "Rule 1",
  "mobile-profile": "Default_Profile",
  "user-groups": [
    "my_group"
  ]
}
```

## Example Responses

### Example 1: add-mobile-access-profile-rule
**Status:** `200 OK`
