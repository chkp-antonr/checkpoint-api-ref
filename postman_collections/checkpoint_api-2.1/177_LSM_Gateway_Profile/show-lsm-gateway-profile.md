# show-lsm-gateway-profile

**Collection:** Web API (version 2.1) > 177 LSM Gateway Profile
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-lsm-gateway-profile`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "gateway_profile"
}
```

## Example Responses

### Example 1: show-lsm-gateway-profile
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "93861c4f-9933-4250-9f3b-7475624e6d07",
  "name": "gateway_profile",
  "type": "lsm-gateway-profile",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1629728256658,
      "iso-8601": "2021-08-23T17:17+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1629728256658,
      "iso-8601": "2021-08-23T17:17+0300"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "Profiles/lsm_profile",
  "groups": [
    {
      "uid": "c7364594-7d60-4931-aac5-369dddb35a83",
      "name": "gw1",
      "type": "lsm-gateway",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "NetworkObjects/ROBO/ROBO_CP",
      "color": "black"
    }
  ],
  "dynamic-ip": false,
  "version": "R77.20",
  "os-name": "Gaia Embedded",
  "firewall": true,
  "vpn": true,
  "application-control": true,
  "url-filtering": true,
  "content-awareness": false,
  "threat-prevention-mode": "custom",
  "ips": false,
  "anti-bot": false,
  "anti-virus": false,
  "threat-emulation": false,
  "threat-extraction": false,
  "identity-awareness": true,
  "save-logs-locally": false,
  "send-alerts-to-server": [],
  "send-logs-to-server": [],
  "send-logs-to-backup-server": []
}
```
