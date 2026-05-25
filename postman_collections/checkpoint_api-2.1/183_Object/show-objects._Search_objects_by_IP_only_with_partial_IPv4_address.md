# show-objects. Search objects by IP only with partial IPv4 address

**Collection:** Web API (version 2.1) > 183 Object
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-objects`

## Description

Searches for the objects using the IP search only with partial IPv4 address.

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
  "filter": "203.0.113",
  "ip-only": true
}
```

## Example Responses

### Example 1: show-objects. Search objects by IP only with partial IPv4 address
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 4,
  "total": 4,
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
      "uid": "f22430e5-16a8-4b1a-b24c-b48bf6ec2d79",
      "name": "net_203.0.113.0",
      "type": "network",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "subnet4": "203.0.113.0",
      "mask-length4": 24,
      "subnet-mask": "255.255.255.0"
    },
    {
      "uid": "0931f471-da08-4fc1-9817-79dd1db21dd3",
      "name": "range_203.0.113.100_203.0.113.200",
      "type": "address-range",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "ipv4-address-first": "203.0.113.100",
      "ipv4-address-last": "203.0.113.200"
    }
  ]
}
```
