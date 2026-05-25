# login to domain

**Collection:** Web API (version 2.1) > 01 Session Management
**Method:** `POST`
**URL:** `{{server}}/v2.1/login-to-domain`

## Description

Login to domain.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "domain": "dom83"
}
```

## Example Responses

### Example 1: login to domain
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "2c01da51-ffcb-4c0b-8149-9a4ba7b9107b",
  "sid": "y0_9jL0hnU0_fRgxzxHKJ6A7j893Wk2mqVFfG8Rute0",
  "url": "https://172.23.78.76:443/web_api",
  "session-timeout": 600,
  "last-login-was-at": {
    "posix": 1604328982661,
    "iso-8601": "2020-11-02T16:56+0200"
  },
  "api-server-version": "1.7.1"
}
```
