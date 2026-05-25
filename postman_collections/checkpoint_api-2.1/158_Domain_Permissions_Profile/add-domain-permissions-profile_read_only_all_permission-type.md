# add-domain-permissions-profile (read only all permission-type)

**Collection:** Web API (version 2.1) > 158 Domain Permissions Profile
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-domain-permissions-profile`

## Description

Add a Domain Permissions Profile with a Read Only All permission-type

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "read profile",
  "permission-type": "read only all"
}
```

## Example Responses

### Example 1: add-domain-permissions-profile (read only all permission-type)
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "9f727ece-4f30-4ed0-b1cf-7aaa7e8d4170",
  "name": "read profile",
  "type": "domain-permissions-profile",
  "domain": {
    "uid": "a0eebc99-afed-4ef8-bb6d-fedfedfedfed",
    "name": "System Data",
    "domain-type": "mds"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1640609614915,
      "iso-8601": "2021-12-27T14:53+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1640609614915,
      "iso-8601": "2021-12-27T14:53+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "General/Role",
  "permission-type": "read only all",
  "edit-common-objects": false,
  "access-control": {
    "show-policy": true,
    "policy-layers": {
      "edit-layers": "by selected profile in a layer editor",
      "firewall": false,
      "app-control-and-url-filtering": false,
      "content-awareness": false,
      "mobile-access": false
    },
    "nat-policy": "read",
    "qos-policy": "read",
    "dlp-policy": "read",
    "geo-control-policy": "read",
    "access-control-objects-and-settings": "read",
    "install-policy": false,
    "app-control-and-url-filtering-update": false
  },
  "endpoint": {
    "manage-policies-and-software-deployment": true,
    "edit-endpoint-policies": false,
    "policies-installation": false,
    "edit-software-deployment": false,
    "software-deployment-installation": false,
    "recovery-media": false,
    "remote-help": false,
    "reset-computer-data": false,
    "authorize-preboot-users": false,
    "allow-executing-push-operations": false
  },
  "events-and-reports": {
    "smart-event": "custom",
    "events": "read",
    "policy": "read",
    "reports": true
  },
  "gateways": {
    "smart-update": "read",
    "lsm-gw-db": "read",
    "manage-provisioning-profiles": "read",
    "vsx-provisioning": false,
    "system-backup": false,
    "system-restore": false,
    "open-shell": false,
    "run-one-time-script": false,
    "run-repository-script": false,
    "manage-repository-scripts": "read"
  },
  "management": {
    "manage-admins": false,
    "manage-sessions": false,
    "high-availability-operations": false,
    "management-api-login": true,
    "cme-operations": "disabled",
    "publish-sessions": false,
    "approve-or-reject-sessions": false
  },
  "monitoring-and-logging": {
    "monitoring": "read",
    "management-logs": "read",
    "track-logs": "read",
    "app-and-url-filtering-logs": true,
    "https-inspection-logs": true,
    "packet-capture-and-forensics": true,
    "show-packet-capture-by-default": true,
    "identities": true,
    "show-identities-by-default": true,
    "dlp-logs-including-confidential-fields": false,
    "manage-dlp-messages": false
  },
  "threat-prevention": {
    "policy-layers": "read",
    "policy-exceptions": "read",
    "profiles": "read",
    "protections": "read",
    "edit-settings": false,
    "install-policy": false,
    "ips-update": false
  },
  "others": {
    "edit-cp-users-db": false,
    "ldap-users-db": "read",
    "user-authority-access": "read",
    "https-inspection": "read",
    "client-certificates": false,
    "user-device-mgmt-conf": "read"
  }
}
```
