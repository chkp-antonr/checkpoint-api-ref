# delete voip-domain-sccp-call-manager

**Collection:** Web API (version 2.1) > 27 VoIP Domain SCCP Call Manager
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-voip-domain-sccp-call-manager`

## Description

Delete existing voip domain sccp call manager.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "sccp1"
}
```

## Example Responses

### Example 1: delete voip-domain-sccp-call-manager
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
