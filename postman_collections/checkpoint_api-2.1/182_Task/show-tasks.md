# show-tasks

**Collection:** Web API (version 2.1) > 182 Task
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-tasks`

## Description

Show all successful tasks initiated by administrator admin1, last updated after date 2018-05-23T08:00:00.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "initiator": "admin1",
  "status": "successful",
  "from-date": "2018-05-23T08:00:00"
}
```

## Example Responses

### Example 1: show-tasks
**Status:** `200 OK`
