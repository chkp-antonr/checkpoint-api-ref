# login (domain)

**Collection:** Web API (version 2.0.1) > 01 Session Management
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/login`

## Description

Login to certain domain

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |

## Request Body

**Mode:** `raw`

```json
{
  "user": "aa",
  "password": "aaaa",
  "domain": "Domain Name"
}
```

## Example Responses

### Example 1: login (domain)
**Status:** `200 OK`

**Body:**
```javascript
{
  "sid": "3MgL4mBU2NfzuFjl5RxlgtRX6Hc8ZYyIR0FP_3RYHAU",
  "url": "https://192.0.2.1:443/web_api",
  "uid": "7586af28-7375-4e19-a052-cb083d918dd0",
  "session-timeout": 600,
  "last-login-was-at": {
    "posix": 1430032266851,
    "iso-8601": "2015-04-26T10:11+0300"
  }
}
```

## Test / Post-response Scripts

```javascript
try {
    var sid = JSON.parse(responseBody).sid;
    postman.setEnvironmentVariable("session", sid);
    tests["login session-id = " + sid] = true;
} catch (e) {}
```
