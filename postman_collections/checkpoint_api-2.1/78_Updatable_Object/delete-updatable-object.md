# delete-updatable-object

**Collection:** Web API (version 2.1) > 78 Updatable Object
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-updatable-object`

## Description

Delete an updatable object

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "CodeBuild US East 1"
}
```

## Example Responses

### Example 1: delete-updatable-object
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
