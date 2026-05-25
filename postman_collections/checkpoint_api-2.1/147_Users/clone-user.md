# clone-user

**Collection:** Web API (version 2.1) > 147 Users
**Method:** `POST`
**URL:** `{{server}}/v2.1/clone-user`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "myuser",
  "authentication-method": "undefined",
  "expiration-date": "2035-01-15",
  "from-hour": "12:00"
}
```

## Example Responses

### Example 1: clone-user
**Status:** `200 OK`
