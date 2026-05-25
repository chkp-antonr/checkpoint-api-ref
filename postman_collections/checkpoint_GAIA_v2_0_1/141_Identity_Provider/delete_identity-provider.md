# delete identity-provider

**Collection:** Web API (version 2.0.1) > 141 Identity Provider
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/delete-identity-provider`

## Description

Delete existing identity provider.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "TestIdp"
}
```

## Example Responses

### Example 1: delete identity-provider
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
