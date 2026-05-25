# set-https-advanced-settings

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
  "bypass-on-failure": "false",
  "bypass-on-client-failure": "false",
  "bypass-under-load.track": "log",
  "site-categorization-allow-mode": "background",
  "server-certificate-validation-actions.block-untrusted": "true",
  "server-certificate-validation-actions.block-revoked": "false",
  "server-certificate-validation-actions.block-expired": "true",
  "blocked-certificate-tracking": "popup alert",
  "bypass-update-services": "true",
  "certificate-pinned-apps-action": "bypass",
  "log-sessions": "true",
  "retrieve-intermediate-ca-certificates": "true",
  "server-certificate-validation-actions.track-errors": "snmp trap alert"
}
```

## Example Responses

### Example 1: set-https-advanced-settings
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "d8fa1329-a1c4-44fd-9bc0-6e4835994425",
  "type": "https-advanced-settings",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1713957198543,
      "iso-8601": "2024-04-24T14:13+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1713462417163,
      "iso-8601": "2024-04-18T20:46+0300"
    },
    "creator": "System"
  },
  "available-actions": {},
  "read-only": true,
  "bypass-on-failure": false,
  "bypass-on-client-failure": false,
  "site-categorization-allow-mode": "background",
  "server-certificate-validation-actions": {
    "block-untrusted": true,
    "block-revoked": false,
    "block-expired": true,
    "track-errors": "snmp trap alert"
  },
  "blocked-certificates": [
    {
      "name": "BlackListed_01C27AA7-9E28-4B80-B02F-6D5C18359BCC",
      "cert-serial-number": "00:b0:b7:13:3e:d0:96:f9:b5:6f:ae:91:c8:74:bd:3a:c0",
      "comments": "login.live.com"
    },
    {
      "name": "BlackListed_0469FE14-751B-4C12-9215-3B5806295B8C",
      "cert-serial-number": "00:e9:02:8b:95:78:e4:15:dc:1a:71:0a:2b:88:15:44:47",
      "comments": "login.skype.com"
    },
    {
      "name": "BlackListed_17880364-603F-4D8D-8B10-30BE164811EE",
      "cert-serial-number": "00:f5:c8:6a:f3:61:62:f1:3a:64:f5:4f:6d:c9:58:7c:06",
      "comments": "www.google.com"
    },
    {
      "name": "BlackListed_362DB435-B2D0-4C68-85DC-1D4EE60FD89D",
      "cert-serial-number": "72:03:21:05:c5:0c:08:57:3d:8e:a5:30:4e:fe:e8:b0",
      "comments": "kuix.de"
    },
    {
      "name": "BlackListed_3A1FAC50-E997-4CBA-A80A-21A20A053737",
      "cert-serial-number": "08:64",
      "comments": "e-islem.kktcmerkezbankasi.org"
    },
    {
      "name": "BlackListed_603F13AB-9648-451E-8ADA-443AEBCF2DFE",
      "cert-serial-number": "39:2a:43:4f:0e:07:df:1f:8a:a3:05:de:34:e0:c2:29",
      "comments": "login.yahoo.com"
    },
    {
      "name": "BlackListed_690C8C66-3F59-4657-8272-7194F0D69A48",
      "cert-serial-number": "00:d8:f3:5f:4e:b7:87:2b:2d:ab:06:92:e3:15:38:2f:b0",
      "comments": "Global Trustee"
    },
    {
      "name": "BlackListed_7CE5028E-F13D-42A7-9DD7-499BB78FCE79",
      "cert-serial-number": "04:7e:cb:e9:fc:a5:5f:7b:d0:9e:ae:36:e1:0c:ae:1e",
      "comments": "mail.google.com"
    },
    {
      "name": "BlackListed_864D1792-5448-4469-A853-08ABE3E2D857",
      "cert-serial-number": "00:92:39:d5:34:8f:40:d1:69:5a:74:54:70:e1:f2:3f:43",
      "comments": "addons.mozilla.org"
    },
    {
      "name": "BlackListed_A2B37A3D-53F9-4A24-AD09-D96272CA1710",
      "cert-serial-number": "00:d7:55:8f:da:f5:f1:10:5b:b2:13:28:2b:70:77:29:a3",
      "comments": "login.yahoo.com"
    },
    {
      "name": "BlackListed_A71D5266-7EF0-42CF-AE9C-409CD4093879",
      "cert-serial-number": "3e:75:ce:d4:6b:69:30:21:21:88:30:ae:86:a8:2a:71",
      "comments": "login.yahoo.com"
    },
    {
      "name": "BlackListed_D6943330-F264-4EDD-A1BC-CEE3BECC8F8E",
      "cert-serial-number": "08:27",
      "comments": "*.EGO.GOV.TR"
    },
    {
      "name": "BlackListed_E869326A-EAD9-4335-AB89-ABF4116A748E",
      "cert-serial-number": "49:33:00:8e",
      "comments": "MCS Holdings"
    }
  ],
  "bypass-update-services": true,
  "certificate-pinned-apps-action": "bypass",
  "retrieve-intermediate-ca-certificates": true,
  "blocked-certificate-tracking": "popup alert",
  "bypass-under-load": {
    "track": "log"
  },
  "log-sessions": true
}
```
