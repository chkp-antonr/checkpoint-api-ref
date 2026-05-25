# delete voip-domain-sip-proxy

**Collection:** Web API (version 2.1) > 25 VoIP Domain SIP Proxy
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-voip-domain-sip-proxy`

## Description

Delete existing voip domain sip proxy.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "sip1"
}
```

## Example Responses

### Example 1: delete voip-domain-sip-proxy
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
