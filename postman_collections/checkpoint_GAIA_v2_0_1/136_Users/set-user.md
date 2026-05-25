# set-user

**Collection:** Web API (version 2.0.1) > 136 Users
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-user`

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

### Example 1: set-user
**Status:** `200 OK`
