# add-user-template

**Collection:** Web API (version 2.0.1) > 139 User Template
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-user-template`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "myusertemplate",
  "expiration-date": "2030-05-30",
  "expiration-by-global-properties": "False"
}
```

## Example Responses

### Example 1: add-user-template
**Status:** `200 OK`
