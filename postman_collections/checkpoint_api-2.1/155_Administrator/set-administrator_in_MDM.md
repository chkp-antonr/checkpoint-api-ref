# set-administrator in MDM

**Collection:** Web API (version 2.1) > 155 Administrator
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-administrator`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "admin",
  "permissions-profile": {
    "add": [
      {
        "domain": "locals",
        "profile": "read only profile"
      },
      {
        "domain": "globals",
        "profile": "read only profile"
      }
    ]
  }
}
```

## Example Responses

### Example 1: set-administrator in MDM
**Status:** `200 OK`
