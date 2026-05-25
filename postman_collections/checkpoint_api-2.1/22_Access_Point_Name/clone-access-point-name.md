# clone-access-point-name

**Collection:** Web API (version 2.1) > 22 Access Point Name
**Method:** `POST`
**URL:** `{{server}}/v2.1/clone-access-point-name`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "myaccesspointname",
  "enforce-end-user-domain": "True",
  "block-traffic-other-end-user-domains": "False",
  "block-traffic-this-end-user-domain": "False"
}
```

## Example Responses

### Example 1: clone-access-point-name
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "f8b6eceb-8670-4c30-b539-b78ddb156164",
  "name": "myaccesspoint",
  "type": "access-point-name",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/AccessPointName",
  "groups": [],
  "apn": "apnname",
  "enforce-end-user-domain": true,
  "end-user-domain": {
    "uid": "b307ca15-2ee8-414a-b261-ac7fb7464736",
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
  "block-traffic-other-end-user-domains": false,
  "block-traffic-this-end-user-domain": false
}
```
