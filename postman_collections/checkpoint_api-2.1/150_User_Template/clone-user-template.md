# clone-user-template

**Collection:** Web API (version 2.1) > 150 User Template
**Method:** `POST`
**URL:** `{{server}}/v2.1/clone-user-template`

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
  "expiration-by-global-properties": "True"
}
```

## Example Responses

### Example 1: clone-user-template
**Status:** `200 OK`
