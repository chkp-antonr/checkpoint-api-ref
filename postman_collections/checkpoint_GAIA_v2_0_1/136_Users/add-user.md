# add-user

**Collection:** Web API (version 2.0.1) > 136 Users
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-user`

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
  "email": "myuser@email.com",
  "expiration-date": "2030-05-30",
  "phone-number": "0501112233",
  "authentication-method": "securid",
  "connect-daily": "True",
  "from-hour": "08:00",
  "to-hour": "17:00",
  "encryption": {
    "enable-ike": "True",
    "enable-public-key": "True"
  }
}
```

## Example Responses

### Example 1: add-user
**Status:** `200 OK`
