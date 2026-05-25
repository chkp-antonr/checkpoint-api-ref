# delete-api-key

**Collection:** Web API (version 2.0.1) > 149 API Key
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/delete-api-key`

## Description

Delete the API key

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "api-key": "FFl8+KF1AJ2Tisac6d0K+w=="
}
```

## Example Responses

### Example 1: delete-api-key
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
