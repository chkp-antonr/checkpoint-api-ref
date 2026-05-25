# show-access-point-name

**Collection:** Web API (version 2.1) > 22 Access Point Name
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-access-point-name`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "myaccesspointname"
}
```

## Example Responses

### Example 1: show-access-point-name
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "7a1856b2-30e5-47cd-8405-038beae67ea0",
  "name": "myaccesspointname",
  "type": "access-point-name",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/AccessPointName",
  "groups": [],
  "apn": "apnname",
  "enforce-end-user-domain": true,
  "end-user-domain": {
    "uid": "9d8e84e9-9a82-460b-82e1-545c6f7750c4",
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
  "block-traffic-other-end-user-domains": true,
  "block-traffic-this-end-user-domain": true
}
```
