# add-domain-permissions-profile

**Collection:** Web API (version 2.0.1) > 147 Domain Permissions Profile
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-domain-permissions-profile`

## Description

Add a Domain Permissions Profile with the default permission-type

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "customized profile"
}
```

## Example Responses

### Example 1: add-domain-permissions-profile
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "20a8ad2e-81f8-481b-96fd-1f13399fd711",
  "name": "customized profile",
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
      "posix": 1640609236052,
      "iso-8601": "2021-12-27T14:47+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1640609236052,
      "iso-8601": "2021-12-27T14:47+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "General/Role",
  "permission-type": "customized",
  "edit-common-objects": false,
  "access-control": {
    "show-policy": true,
    "policy-layers": {
      "edit-layers": "by software blades",
      "firewall": true,
      "app-control-and-url-filtering": true,
      "content-awareness": true,
      "mobile-access": true
    },
    "nat-policy": "write",
    "qos-policy": "write",
    "dlp-policy": "write",
    "geo-control-policy": "write",
    "access-control-objects-and-settings": "write",
    "install-policy": true,
    "app-control-and-url-filtering-update": true
  },
  "endpoint": {
    "manage-policies-and-software-deployment": true,
    "edit-endpoint-policies": true,
    "policies-installation": true,
    "edit-software-deployment": true,
    "software-deployment-installation": true,
    "recovery-media": true,
    "remote-help": true,
    "reset-computer-data": true,
    "authorize-preboot-users": true,
    "allow-executing-push-operations": true
  },
  "events-and-reports": {
    "smart-event": "custom",
    "events": "write",
    "policy": "write",
    "reports": true
  },
  "gateways": {
    "smart-update": "read",
    "lsm-gw-db": "disabled",
    "manage-provisioning-profiles": "disabled",
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
    "high-availability-operations": true,
    "management-api-login": true,
    "cme-operations": "disabled",
    "publish-sessions": true,
    "approve-or-reject-sessions": false
  },
  "monitoring-and-logging": {
    "monitoring": "write",
    "management-logs": "write",
    "track-logs": "write",
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
    "policy-layers": "write",
    "edit-layers": "all",
    "policy-exceptions": "write",
    "profiles": "write",
    "protections": "write",
    "edit-settings": true,
    "install-policy": true,
    "ips-update": true
  },
  "others": {
    "edit-cp-users-db": true,
    "ldap-users-db": "write",
    "user-authority-access": "write",
    "https-inspection": "write",
    "client-certificates": true,
    "user-device-mgmt-conf": "read"
  }
}
```
