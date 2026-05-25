# show-user-templates

**Collection:** Web API (version 2.1) > 150 User Template
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-user-templates`

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

### Example 1: show-user-templates
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 1,
  "total": 1,
  "objects": [
    {
      "uid": "04f57557-f61c-a842-8cf8-b32eac08088a",
      "name": "Default",
      "type": "user-template",
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
        "posix": 1924898400000,
        "iso-8601": "2030-12-31T00:00+0200"
      },
      "authentication-method": "undefined",
      "allowed-locations": {
        "sources": [
          "97aeb369-9aea-11d5-bd16-0090272ccb30"
        ],
        "destinations": [
          "97aeb369-9aea-11d5-bd16-0090272ccb30"
        ]
      },
      "from-hour": "00:00",
      "to-hour": "23:59",
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
      "expiration-by-global-properties": true
    }
  ]
}
```
