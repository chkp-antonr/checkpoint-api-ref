# update-updatable-objects-repository-content

**Collection:** Web API (version 2.0.1) > 66 Updatable Objects Repository
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/update-updatable-objects-repository-content`

## Description

Update the objects in the Updatable Objects repository. Use the show-task command to check the progress of the task.

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

### Example 1: update-updatable-objects-repository-content
**Status:** `200 OK`

**Body:**
```javascript
{
  "task-id": "01234567-89ab-cdef-a930-8c37a59972b3"
}
```
