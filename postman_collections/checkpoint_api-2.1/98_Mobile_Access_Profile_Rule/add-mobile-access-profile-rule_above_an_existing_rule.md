# add-mobile-access-profile-rule above an existing rule

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
  "position": {
    "above": "Rule 1"
  },
  "name": "One before the last",
  "mobile-profile": "Default_Profile"
}
```

## Example Responses

### Example 1: add-mobile-access-profile-rule above an existing rule
**Status:** `200 OK`
