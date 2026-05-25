# show-provisioning-profile

**Collection:** Web API (version 2.0.1) > 162 Provisioning Profile
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-provisioning-profile`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "prv_gaia_profile"
}
```

## Example Responses

### Example 1: show-provisioning-profile
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "ea51c98a-65aa-3f43-bca8-582c379226c8",
  "name": "SMBCluster",
  "type": "provisioning-profile",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "dns": {
    "primary-server": "194.29.40.221",
    "secondary-server": "194.29.40.220",
    "tertiary-server": "",
    "dns-proxy": true,
    "servers-configuration-mode": "manual",
    "manage-settings": "locally on the device",
    "override-settings": "allowed"
  },
  "hosts": {
    "manage-settings": "centrally from this application",
    "override-settings": "allowed"
  },
  "domain-name": {
    "manage-settings": "centrally from this application",
    "override-settings": "allowed"
  },
  "radius": {
    "enabled": false,
    "allow-administrators-from-specific-radius-group-only": false,
    "manage-settings": "centrally from this application",
    "override-settings": "allowed"
  },
  "hotspot": {
    "enabled": false,
    "display-terms-of-use": false,
    "require-authentication": false,
    "allow-users-from-specific-group": false,
    "manage-settings": "centrally from this application",
    "override-settings": "allowed"
  },
  "configuration-script": {
    "manage-settings": "centrally from this application",
    "override-settings": "allowed"
  },
  "groups": [
    {
      "uid": "a5a615ca-ed33-e045-970e-4511a931a215",
      "name": "C_SMB_68_34",
      "type": "",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "Unknown"
    },
    {
      "uid": "615f88ce-5962-8146-9d60-e2b9647ff974",
      "name": "C_SMB_68_29",
      "type": "",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "Unknown"
    }
  ],
  "comments": "",
  "icon": "NetworkObjects/ROBO/Profile_Provisioning",
  "tags": [],
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1629971663134,
      "iso-8601": "2021-08-26T12:54+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1629800112921,
      "iso-8601": "2021-08-24T13:15+0300"
    },
    "creator": "aa"
  },
  "read-only": false
}
```
