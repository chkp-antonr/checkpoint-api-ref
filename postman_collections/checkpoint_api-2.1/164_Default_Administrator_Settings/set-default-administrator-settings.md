# set-default-administrator-settings

**Collection:** Web API (version 2.1) > 164 Default Administrator Settings
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-default-administrator-settings`

## Description

Edit default administrator settings.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "expiration-type": "expiration date",
  "expiration-date": "2025-06-23",
  "indicate-expiration-in-admin-view": false,
  "notify-expiration-to-admin": true,
  "days-to-notify-expiration-to-admin": 5
}
```

## Example Responses

### Example 1: set-default-administrator-settings
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "57bba962-ea49-4990-a289-380f29d48434",
  "type": "default-administrator-settings",
  "domain": {
    "uid": "a0eebc99-afed-4ef8-bb6d-fedfedfedfed",
    "name": "System Data",
    "domain-type": "mds"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1738764688338,
      "iso-8601": "2025-02-05T16:11+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1738588307699,
      "iso-8601": "2025-02-03T15:11+0200"
    },
    "creator": "System"
  },
  "authentication-method": "check point password",
  "expiration-type": "expiration date",
  "expiration-date": {
    "posix": 1750626000000,
    "iso-8601": "2025-06-23T00:00+0300"
  },
  "expiration-period": 10,
  "expiration-period-time-units": "months",
  "indicate-expiration-in-admin-view": false,
  "notify-expiration-to-admin": true,
  "days-to-indicate-expiration-in-admin-view": 20,
  "days-to-notify-expiration-to-admin": 5
}
```
