# delete voip-domain-h323-gateway

**Collection:** Web API (version 2.1) > 29 VoIP Domain H.323 Gateway
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-voip-domain-h323-gateway`

## Description

Delete existing voip domain h323 gateway.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "vdhgw1"
}
```

## Example Responses

### Example 1: delete voip-domain-h323-gateway
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
