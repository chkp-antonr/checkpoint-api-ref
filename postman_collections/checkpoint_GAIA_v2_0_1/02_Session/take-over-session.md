# take-over-session

**Collection:** Web API (version 2.0.1) > 02 Session
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/take-over-session`

## Description

Take over an existing session with UID "41e821a0-3720-11e3-aa6e-0800200c9fde".

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
  "disconnect-active-session": true
}
```

## Example Responses

### Example 1: take-over-session
**Status:** `200 OK`
