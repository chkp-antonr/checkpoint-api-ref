# disconnect-cloud-services

**Collection:** Web API (version 2.1) > 174 Cloud Services
**Method:** `POST`
**URL:** `{{server}}/v2.1/disconnect-cloud-services`

## Description

Disconnect the management server from Check Point Smart-1 Cloud services.

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

### Example 1: disconnect-cloud-services
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
