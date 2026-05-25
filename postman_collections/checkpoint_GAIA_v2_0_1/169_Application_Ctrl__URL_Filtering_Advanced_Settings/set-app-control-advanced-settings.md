# set-app-control-advanced-settings

**Collection:** Web API (version 2.0.1) > 169 Application Ctrl & URL Filtering Advanced Settings
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-app-control-advanced-settings`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "internal-error-fail-mode": "block connections",
  "url-filtering-settings.categorize-https-websites": "true",
  "url-filtering-settings.enforce-safe-search": "true",
  "url-filtering-settings.categorize-cached-and-translated-pages": "false",
  "web-browsing-services.add.1": "AH",
  "match-application-on-any-port": "true",
  "enable-web-browsing": "true",
  "httpi-non-standard-ports": "true",
  "block-request-when-web-service-is-unavailable": "true",
  "website-categorization-mode": "custom",
  "custom-categorization-settings.url-filtering-mode": "hold",
  "custom-categorization-settings.social-network-widgets-mode": "background",
  "categorize-social-network-widgets": "true"
}
```

## Example Responses

### Example 1: set-app-control-advanced-settings
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "0d9fcf03-ba25-4ee3-9080-f555f91b5716",
  "type": "app-control-advanced-settings",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1678712561818,
      "iso-8601": "2023-03-13T15:02+0200"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1675750866427,
      "iso-8601": "2023-02-07T08:21+0200"
    },
    "creator": "System"
  },
  "available-actions": {
    "edit": "true",
    "delete": "true",
    "clone": "true"
  },
  "read-only": false,
  "internal-error-fail-mode": "block connections",
  "url-filtering-settings": {
    "categorize-https-websites": true,
    "enforce-safe-search": true,
    "categorize-cached-and-translated-pages": false
  },
  "session-unification-timeout": 180,
  "web-browsing-services": [
    {
      "uid": "97aeb3d0-9aea-11d5-bd16-0090272ccb30",
      "name": "ftp",
      "type": "service-tcp",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      },
      "icon": "Protocols/FTP",
      "color": "forest green",
      "port": "21"
    },
    {
      "uid": "97aeb3d4-9aea-11d5-bd16-0090272ccb30",
      "name": "http",
      "type": "service-tcp",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      },
      "icon": "Protocols/HTTP",
      "color": "forest green",
      "port": "80"
    },
    {
      "uid": "2a2ca572-fbe7-4e7f-92e4-164f5b4fded1",
      "name": "HTTP_and_HTTPS_proxy",
      "type": "service-tcp",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      },
      "icon": "Services/TCPService",
      "color": "black",
      "port": "8080"
    },
    {
      "uid": "97aeb443-9aea-11d5-bd16-0090272ccb30",
      "name": "https",
      "type": "service-tcp",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      },
      "icon": "Protocols/HTTP",
      "color": "red",
      "port": "443"
    },
    {
      "uid": "8eddeaa0-259d-448f-95b6-490a39f55962",
      "name": "HTTP_proxy",
      "type": "service-tcp",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      },
      "icon": "Protocols/HTTP",
      "color": "orange",
      "port": "8080"
    },
    {
      "uid": "97aeb422-9aea-11d5-bd16-0090272ccb30",
      "name": "AH",
      "type": "service-other",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      },
      "icon": "Services/OtherService",
      "color": "cyan"
    }
  ],
  "match-application-on-any-port": true,
  "enable-web-browsing": true,
  "httpi-non-standard-ports": true,
  "unify-connections": false,
  "issue-separate-log-per-domain": true,
  "block-request-when-web-service-is-unavailable": true,
  "website-categorization-mode": "custom",
  "custom-categorization-settings": {
    "url-filtering-mode": "hold",
    "social-network-widgets-mode": "background"
  },
  "categorize-social-network-widgets": true
}
```
