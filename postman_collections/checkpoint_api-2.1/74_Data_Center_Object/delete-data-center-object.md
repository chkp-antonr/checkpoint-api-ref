# delete-data-center-object

**Collection:** Web API (version 2.1) > 74 Data Center Object
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-data-center-object`

## Description

delete-data-center-object

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "VM1 mgmt name"
}
```

## Example Responses

### Example 1: delete-data-center-object
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
