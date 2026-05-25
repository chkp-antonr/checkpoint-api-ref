# show-services-sctp

**Collection:** Web API (version 2.0.1) > 72 Service SCTP
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-services-sctp`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "limit": 50,
  "offset": 0,
  "details-level": "standard"
}
```

## Example Responses

### Example 1: show-services-sctp
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 1,
  "total": 1,
  "objects": [
    {
      "uid": "855ef7a1-b44f-4587-9c36-3f4a8c5d12b9",
      "name": "New_SCTP_Service_5",
      "type": "service-sctp",
      "domain": {
        "domain-type": "domain",
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User"
      }
    }
  ]
}
```
