# login with API key

**Collection:** Web API (version 2.1) > 01 Session Management
**Method:** `POST`
**URL:** `{{server}}/v2.1/login`

## Description

Login with API key without user and password.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |

## Request Body

**Mode:** `raw`

```json
{
  "api-key": "FFl8+KF1AJ2Tisac6d0K+w=="
}
```

## Example Responses

### Example 1: login with API key
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "1c7d98ea-89f9-43fd-8cd1-db291c2200cd",
  "sid": "HzlgNlKqNOKT6UKuFCSo3xZnFTA44IYTFlEiE2PLtL4",
  "url": "https://172.23.78.79:443/web_api",
  "session-timeout": 600,
  "api-server-version": "1.5"
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
