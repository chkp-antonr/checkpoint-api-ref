# set-https-advanced-settings updating existing blocked certificate by its name

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
  "blocked-certificates.update.name": "bbbb",
  "blocked-certificates.update.cert-serial-number": "bb:bb:bb",
  "blocked-certificates.update.comments": "bbb"
}
```

## Example Responses

### Example 1: set-https-advanced-settings updating existing blocked certificate by its name
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
      "cert-serial-number": "bb:bb:bb",
      "comment": "bbb"
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
