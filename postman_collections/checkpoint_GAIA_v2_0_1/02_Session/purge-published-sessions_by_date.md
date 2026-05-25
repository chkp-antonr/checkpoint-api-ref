# purge-published-sessions by date

**Collection:** Web API (version 2.0.1) > 02 Session
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/purge-published-sessions`

## Description

Purge all sessions published prior the date 2018-07-29T12:00:00. Sessions published until this date are preserved.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "preserve-to-date": "2018-07-29T12:00:00"
}
```

## Example Responses

### Example 1: purge-published-sessions by date
**Status:** `200 OK`
