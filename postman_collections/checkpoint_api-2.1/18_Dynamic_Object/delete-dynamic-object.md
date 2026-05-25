# delete-dynamic-object

**Collection:** Web API (version 2.1) > 18 Dynamic Object
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-dynamic-object`

## Description

Delete existing dynamic object

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "Dynamic_Object_2"
}
```

## Example Responses

### Example 1: delete-dynamic-object
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
