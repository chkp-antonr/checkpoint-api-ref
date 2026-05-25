# show-users

**Collection:** Web API (version 2.0.1) > 136 Users
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-users`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "details-level": "full"
}
```

## Example Responses

### Example 1: show-users
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 1,
  "total": 1,
  "objects": [
    {
      "uid": "459d1689-9aad-40b6-9da3-56d7bc6eb857",
      "name": "myuser",
      "type": "user",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "tags": [],
      "read-only": false,
      "comments": "",
      "color": "black",
      "icon": "Objects/user",
      "groups": [],
      "expiration-date": {
        "posix": 1906318800000,
        "iso-8601": "2030-05-30T00:00+0300"
      },
      "authentication-method": "securid",
      "allowed-locations": {
        "sources": [
          "97aeb369-9aea-11d5-bd16-0090272ccb30"
        ],
        "destinations": [
          "97aeb369-9aea-11d5-bd16-0090272ccb30"
        ]
      },
      "from-hour": "08:00",
      "to-hour": "17:00",
      "connect-on-days": [
        "Sunday",
        "Monday",
        "Tuesday",
        "Wednesday",
        "Thursday",
        "Friday",
        "Saturday"
      ],
      "connect-daily": true,
      "encryption": {
        "ike": true,
        "shared-secret": false,
        "public-key": true
      },
      "email": "myuser@email.com",
      "phone-number": "0501112233"
    }
  ]
}
```
