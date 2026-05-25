# purge-published-sessions by count

**Collection:** Web API (version 2.0.1) > 02 Session
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/purge-published-sessions`

## Description

Purge all sessions except the specified number of newest sessions to preserve.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "number-of-sessions-to-preserve": "10"
}
```

## Example Responses

### Example 1: purge-published-sessions by count
**Status:** `200 OK`
