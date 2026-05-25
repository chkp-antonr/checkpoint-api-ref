# login to last published session

**Collection:** Web API (version 2.1) > 01 Session Management
**Method:** `POST`
**URL:** `{{server}}/v2.1/login`

## Description

Login to last published session

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
  "enter-last-published-session": true
}
```

## Example Responses

### Example 1: login to last published session
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "0bd70128-4e5b-414b-9c98-fa00264507d2",
  "sid": "a0-bI7gXp1IBVMDFIXkrheSDEbQOhqV3_XF2qRaY5ac",
  "url": "https://172.23.78.57:4434/web_api",
  "session-timeout": 600,
  "last-login-was-at": {
    "posix": 1469005943038,
    "iso-8601": "2016-07-20T12:12+0300"
  },
  "api-server-version": "1.1"
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
