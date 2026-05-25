# continue-session-in-smartconsole

**Collection:** Web API (version 2.1) > 02 Session
**Method:** `POST`
**URL:** `{{server}}/v2.1/continue-session-in-smartconsole`

## Description

Continue an existing API session who's UID is "bae159e7-d3ef-44ab-a8a8-ea3ce7ee25a5" in SmartConsole.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "uid": "bae159e7-d3ef-44ab-a8a8-ea3ce7ee25a5"
}
```

## Example Responses

### Example 1: continue-session-in-smartconsole
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
