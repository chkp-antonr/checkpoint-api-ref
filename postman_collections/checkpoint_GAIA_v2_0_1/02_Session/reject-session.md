# reject-session

**Collection:** Web API (version 2.0.1) > 02 Session
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/reject-session`

## Description

Reject session with UID "41e821a0-3720-11e3-aa6e-0800200c9fde" and return it to the submitter administrator.

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
  "comments": "Typo in host name"
}
```

## Example Responses

### Example 1: reject-session
**Status:** `200 OK`
