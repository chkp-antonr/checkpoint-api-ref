# login to system domain

**Collection:** Web API (version 2.1) > 01 Session Management
**Method:** `POST`
**URL:** `{{server}}/v2.1/login`

## Description

Login to system domain

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
  "domain": "System Data"
}
```

## Example Responses

### Example 1: login to system domain
**Status:** `200 OK`

**Body:**
```javascript
{
  "sid": "FGUjxwAVtaHZewYzap4IveDp1STl50iAdxuR3v6rkRo",
  "url": "https://192.0.2.1:443/web_api",
  "uid": "a50785cc-db67-4149-8d61-eb4bef1c4348",
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
