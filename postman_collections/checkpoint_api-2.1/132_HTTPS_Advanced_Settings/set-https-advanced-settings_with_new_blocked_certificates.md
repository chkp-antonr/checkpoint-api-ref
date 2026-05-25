# set-https-advanced-settings with new blocked certificates

**Collection:** Web API (version 2.1) > 132 HTTPS Advanced Settings
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-https-advanced-settings`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "blocked-certificates.add.1.name": "aaaa",
  "blocked-certificates.add.1.cert-serial-number": "aa:aa",
  "blocked-certificates.add.1.comments": "aa",
  "blocked-certificates.add.2.name": "cccc",
  "blocked-certificates.add.2.cert-serial-number": "cc:cc",
  "blocked-certificates.add.2.comments": "cc"
}
```

## Example Responses

### Example 1: set-https-advanced-settings with new blocked certificates
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
      "name": "cccc",
      "cert-serial-number": "cc:cc",
      "comment": "cc"
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
