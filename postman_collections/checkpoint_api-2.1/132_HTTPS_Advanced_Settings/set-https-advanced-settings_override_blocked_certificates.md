# "set-https-advanced-settings override blocked certificates"

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
  "blocked-certificates.1.name": "bbbb",
  "blocked-certificates.1.cert-serial-number": "bb:bb",
  "blocked-certificates.1.comments": "bb",
  "blocked-certificates.2.name": "dddd",
  "blocked-certificates.2.cert-serial-number": "dd:dd",
  "blocked-certificates.2.comments": "dd"
}
```

## Example Responses

### Example 1: "set-https-advanced-settings override blocked certificates"
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
