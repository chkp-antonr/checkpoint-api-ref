# show-logs with paging

**Collection:** Web API (version 2.0.1) > 156 Logs
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-logs`

## Description

Querying for the next page of logs. To be able to use the show logs with paging command, you must include the session id that was used in the show logs command.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "query-id": "aa_be383957-9167-4ca3-b101-a25bc0fbec1c"
}
```

## Example Responses

### Example 1: show-logs with paging
**Status:** `200 OK`
