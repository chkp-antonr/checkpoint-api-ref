# show-interoperable-devices

**Collection:** Web API (version 2.1) > 13 Interoperable Device
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-interoperable-devices`

## Description

Shows all interoperable devices

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{}
```

## Example Responses

### Example 1: show-interoperable-devices
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 2,
  "total": 2,
  "objects": [
    {
      "uid": "5e42446c-c24f-4626-a223-c9cb181cd4ff",
      "name": "FirstInteroperableDevice",
      "type": "interop",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "NetworkObjects/gateway",
      "color": "black",
      "ipv4-address": "192.168.1.6"
    },
    {
      "uid": "b557125d-448a-40ab-9fae-77c595a9bfc2",
      "name": "SecondInteroperableDevice",
      "type": "interop",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "NetworkObjects/gateway",
      "color": "black",
      "ipv4-address": "192.168.1.7"
    }
  ]
}
```
