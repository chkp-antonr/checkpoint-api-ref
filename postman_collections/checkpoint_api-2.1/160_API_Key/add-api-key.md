# add-api-key

**Collection:** Web API (version 2.1) > 160 API Key
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-api-key`

## Description

Add API key for admin

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "admin-name": "admin"
}
```

## Example Responses

### Example 1: add-api-key
**Status:** `200 OK`

**Body:**
```javascript
{
  "api-key": "FFl8+KF1AJ2Tisac6d0K+w=="
}
```
