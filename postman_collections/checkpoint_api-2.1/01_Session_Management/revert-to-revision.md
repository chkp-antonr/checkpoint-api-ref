# revert-to-revision

**Collection:** Web API (version 2.1) > 01 Session Management
**Method:** `POST`
**URL:** `{{server}}/v2.1/revert-to-revision`

## Description

Revert the Management Database to the selected revision.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "to-session": "d49ed10c-649a-476a-8e80-8282eda00e15"
}
```

## Example Responses

### Example 1: revert-to-revision
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-cdef-a930-8c37ab9972b3"
}
```
