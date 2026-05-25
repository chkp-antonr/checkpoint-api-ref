# show-dns-domains

**Collection:** Web API (version 2.0.1) > 20 DNS Domain
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-dns-domains`

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

### Example 1: show-dns-domains
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 1,
  "total": 1,
  "objects": [
    {
      "uid": "ab7aa902-ccac-4278-b4eb-c140c07c6170",
      "name": ".www.example.com",
      "type": "dns-domain",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    }
  ]
}
```
