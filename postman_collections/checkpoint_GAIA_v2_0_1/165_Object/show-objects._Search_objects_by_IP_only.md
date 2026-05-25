# show-objects. Search objects by IP only

**Collection:** Web API (version 2.0.1) > 165 Object
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-objects`

## Description

Searches for the objects using the IP search only.

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
  "type": "object",
  "filter": "192.0.2.100",
  "ip-only": true
}
```

## Example Responses

### Example 1: show-objects. Search objects by IP only
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 3,
  "total": 3,
  "objects": [
    {
      "uid": "387e088c-3fa3-433d-816f-d3fe3bfeabd6",
      "name": "All_Internet",
      "type": "address-range",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "ipv4-address-first": "0.0.0.0",
      "ipv4-address-last": "255.255.255.255"
    },
    {
      "uid": "0e16cffc-439a-4e3d-951d-7cf00faf4418",
      "name": "h_192.0.2.100_with_iface_203.0.113",
      "type": "host",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "ipv4-address": "192.0.2.100"
    },
    {
      "uid": "fa27706e-3d95-4abc-9601-26b42c07060f",
      "name": "net_192.0.2.0",
      "type": "network",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "subnet4": "192.0.2.0",
      "mask-length4": 24,
      "subnet-mask": "255.255.255.0"
    }
  ]
}
```
