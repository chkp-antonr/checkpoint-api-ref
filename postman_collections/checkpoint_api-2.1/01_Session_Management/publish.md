# publish

**Collection:** Web API (version 2.1) > 01 Session Management
**Method:** `POST`
**URL:** `{{server}}/v2.1/publish`

## Description

Publish the last changes. Use the show-task command to check the progress of the task.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{}
```

## Example Responses

### Example 1: publish
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-cdef-a930-8c37a59972b3"
}
```
