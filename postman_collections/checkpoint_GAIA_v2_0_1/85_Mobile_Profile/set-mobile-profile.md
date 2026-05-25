# set-mobile-profile

**Collection:** Web API (version 2.0.1) > 85 Mobile Profile
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-mobile-profile`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Mobile Profile",
  "new-name": "Mobile Profile",
  "data-leak-prevention": {
    "share-protected-extension": "word documents"
  }
}
```

## Example Responses

### Example 1: set-mobile-profile
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "d81c95ed-bb8b-47de-98f0-3e2397eb1035",
  "name": "Mobile Profile",
  "type": "mobile-profile",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "client-customization": {
    "app-theme-color-light": "fc037b",
    "app-theme-color-dark": "fc037b",
    "allow-mail": true,
    "allow-secure-chat": true,
    "allow-calendar": true,
    "allow-contacts": true,
    "allow-tasks": true,
    "allow-notes-sync": true,
    "allow-saved-file-apps": true,
    "certificate-expire-message": ""
  },
  "security": {
    "session-timeout": 1,
    "session-timeout-unit": "weeks",
    "activate-passcode-lock": true,
    "passcode-profile": {
      "uid": "d828d7c4-78be-420e-984e-ce676c54b667",
      "name": "Restrictive",
      "type": "passcode-profile",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "MobileProfile/passcode_policy",
      "color": "firebrick"
    },
    "allow-store-credentials": false,
    "report-jailbroken": true,
    "block-jailbroken": "none",
    "block-3rd-party-keyboard": false,
    "hide-ssl-connect-anyway-button": false
  },
  "applications": {
    "enable-print-mails": false,
    "max-attachments-size": 5,
    "enable-microsoft-365": false,
    "azure-ad-endpoint": "",
    "service-root-endpoint": "",
    "tenant-id": "",
    "app-id": "",
    "mail-from-the-last": 14,
    "mail-from-the-last-unit": "days",
    "calendar-from-the-last": 1,
    "calendar-from-the-last-unit": "months",
    "calendar-to-the-following": 1,
    "calendar-to-the-following-unit": "months",
    "synchronize-contacts": "mail srv to app",
    "allow-push-notification": true,
    "allow-calendar-sync": false,
    "allow-contacts-from-global-address-list": true,
    "allow-contacts-from-local-phone": true,
    "save-local-web-cache": false,
    "allow-caching-docsec-credentials": true,
    "allow-caching-docsec-keys": true
  },
  "data-leak-prevention": {
    "share-protected-extension": [
      "word documents"
    ],
    "share-unprotected-extension": [],
    "open-extension-with-external-app": [
      "any file"
    ],
    "accept-protected-file-extensions": [
      "any file"
    ],
    "accept-unprotected-file-extensions": [
      "any file"
    ],
    "block-screenshot": false,
    "allow-copy-paste": true,
    "block-forward-attachments": false,
    "allowed-domains-forward-attachment": "",
    "offer-capsule-as-viewer": true,
    "allow-taking-photos-and-videos": true,
    "allow-import-from-gallery": true
  },
  "harmony-mobile": {
    "enable-harmony-mobile-application": false,
    "enforcement-policy": "not enforced",
    "enforcement-action": "warn",
    "enforcement-message": "",
    "enable-harmony-mobile-sdk": false,
    "harmony-mobile-sdk-license": "",
    "compromised-behavior": "block",
    "malware-behavior": "block",
    "man-in-the-middle-attack": "notify",
    "os-integrity-compromised": "block",
    "suspicious-app": "block",
    "suspicious-enterprise-certificate": "notify"
  },
  "comments": "",
  "color": "black",
  "icon": "Profiles/profile",
  "tags": [],
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1682859234791,
      "iso-8601": "2023-04-30T15:53+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1682858894604,
      "iso-8601": "2023-04-30T15:48+0300"
    },
    "creator": "aa"
  },
  "read-only": true,
  "available-actions": {}
}
```
