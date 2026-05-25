# delete voip-domain-h323-gatekeeper

**Collection:** Web API (version 2.1) > 28 VoIP Domain H.323 Gatekeeper
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-voip-domain-h323-gatekeeper`

## Description

Delete existing voip domain h323 gatekeeper.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "vdhg1"
}
```

## Example Responses

### Example 1: delete voip-domain-h323-gatekeeper
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
