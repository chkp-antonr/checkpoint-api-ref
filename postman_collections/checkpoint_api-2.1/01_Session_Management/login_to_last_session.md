# login to last session

**Collection:** Web API (version 2.1) > 01 Session Management
**Method:** `POST`
**URL:** `{{server}}/v2.1/login`

## Description

Login to the last session

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
  "continue-last-session": true
}
```

## Example Responses

### Example 1: login to last session
**Status:** `200 OK`

**Body:**
```javascript
{
  "sid": "tdv_CAG-Lm04wSsMxO43NQhsKipw9MT-l-YFG9Z79AA",
  "url": "https://192.0.2.1:443/web_api",
  "uid": "040cdfe8-e967-407c-af34-2c69884f8e9f",
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
