# verify-revert

**Collection:** Web API (version 2.1) > 01 Session Management
**Method:** `POST`
**URL:** `{{server}}/v2.1/verify-revert`

## Description

Verify the Management Database can revert to the selected revision.

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

### Example 1: verify-revert
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-cdef-a930-8c37ac9972b3"
}
```
