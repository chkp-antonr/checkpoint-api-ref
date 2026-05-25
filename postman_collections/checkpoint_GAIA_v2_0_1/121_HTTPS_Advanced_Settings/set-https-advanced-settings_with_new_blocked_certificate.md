# set-https-advanced-settings with new blocked certificate

**Collection:** Web API (version 2.0.1) > 121 HTTPS Advanced Settings
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-https-advanced-settings`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "blocked-certificates.add.name": "aaaa",
  "blocked-certificates.add.cert-serial-number": "aa:aa",
  "blocked-certificates.add.comments": "aa"
}
```

## Example Responses

### Example 1: set-https-advanced-settings with new blocked certificate
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "a47636b4-dd8f-48b6-9696-0ceaa39d4d56",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1673427367283,
      "iso-8601": "2023-01-11T10:56+0200"
    },
    "last-modifier": "System",
    "creation-time": {
      "posix": 1673427367283,
      "iso-8601": "2023-01-11T10:56+0200"
    },
    "creator": "System"
  },
  "available-actions": {
    "edit": "true",
    "delete": "true",
    "clone": "false"
  },
  "read-only": false,
  "bypass-on-failure": true,
  "bypass-on-client-failure": true,
  "site-categorization-allow-mode": "hold",
  "deny-untrusted-server-cert": false,
  "deny-expired-server-cert": false,
  "blocked-certificates": [
    {
      "name": "aaaa",
      "cert-serial-number": "aa:aa",
      "comment": "aa"
    },
    {
      "name": "bbbb",
      "cert-serial-number": "bb:bb",
      "comment": "bb"
    },
    {
      "name": "dddd",
      "cert-serial-number": "dd:dd",
      "comment": "dd"
    }
  ],
  "deny-revoked-server-cert": true
}
```
