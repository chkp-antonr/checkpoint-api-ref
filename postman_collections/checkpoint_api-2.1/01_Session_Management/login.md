# login

**Collection:** Web API (version 2.1) > 01 Session Management
**Method:** `POST`
**URL:** `{{server}}/v2.1/login`

## Description

Login request to receive session token.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |

## Request Body

**Mode:** `raw`

```json
{
  "user": "aa",
  "password": "aaaa"
}
```

## Example Responses

### Example 1: login
**Status:** `200 OK`

**Body:**
```javascript
{
  "sid": "97BVpRfN4j81ogN-V2XqGYmw3DDwIhoSn0og8PiKDiM",
  "url": "https://192.0.2.1:443/web_api",
  "uid": "7a13a360-9b24-40d7-acd3-5b50247be33e",
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
