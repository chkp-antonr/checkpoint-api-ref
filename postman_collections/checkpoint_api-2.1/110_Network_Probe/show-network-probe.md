# show-network-probe

**Collection:** Web API (version 2.1) > 110 Network Probe
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-network-probe`

## Description

Displays a Network Probe.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "probe_GW1"
}
```

## Example Responses

### Example 1: show-network-probe
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "68712ad4-fc46-4b28-99c4-3a9580aa052a",
  "name": "probe_GW1",
  "type": "network-probe",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1667409414222,
      "iso-8601": "2022-11-02T19:16+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1667408936755,
      "iso-8601": "2022-11-02T19:08+0200"
    },
    "creator": "WEB_API"
  },
  "available-actions": {
    "edit": "true",
    "delete": "true",
    "clone": "false"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/NetworkProbe",
  "install-on": [
    {
      "uid": "55cacbf7-9cff-574b-8511-a6060c2007c1",
      "name": "vpnmon-ivory-t569-main-take-1",
      "type": "simple-gateway",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "NetworkObjects/management",
      "color": "black"
    }
  ],
  "protocol": "icmp",
  "interval": 10,
  "timeout": 20,
  "icmp-options": {
    "source": "1.1.1.1",
    "destination": "2.2.2.2"
  },
  "http-options": {}
}
```
