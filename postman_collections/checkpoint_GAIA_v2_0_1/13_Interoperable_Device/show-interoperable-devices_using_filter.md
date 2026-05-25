# show-interoperable-devices using filter

**Collection:** Web API (version 2.0.1) > 13 Interoperable Device
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-interoperable-devices`

## Description

Shows all interoperable devices with a specific filter

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "filter": "InteroperableDevice_"
}
```

## Example Responses

### Example 1: show-interoperable-devices using filter
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 2,
  "total": 2,
  "objects": [
    {
      "uid": "0686d3da-01e6-48b6-96f8-595661d0fa6d",
      "name": "InteroperableDevice_1",
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
      "uid": "e6e9cb1d-4745-4cc6-8c81-3f59e4e3e4a1",
      "name": "InteroperableDevice_2",
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
