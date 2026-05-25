# delete-opsec-application

**Collection:** Web API (version 2.0.1) > 30 OPSEC Application
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/delete-opsec-application`

## Description

Deletes an OPSEC Application

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "MySecondOpsecApplication"
}
```

## Example Responses

### Example 1: delete-opsec-application
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
