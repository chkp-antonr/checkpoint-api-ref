# show-content-awareness-advanced-settings

**Collection:** Web API (version 2.1) > 188 Content Awareness Advanced Settings
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-threat-advanced-settings`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{}
```

## Example Responses

### Example 1: show-content-awareness-advanced-settings
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "b086052c-8ef5-4646-bcb0-0512413d10e1",
  "type": "content-awareness-advanced-settings",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1678783954585,
      "iso-8601": "2023-03-14T10:52+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1675750869050,
      "iso-8601": "2023-02-07T08:21+0200"
    },
    "creator": "System"
  },
  "available-actions": {
    "edit": "true",
    "delete": "false",
    "clone": "true"
  },
  "read-only": false,
  "internal-error-fail-mode": "block connections",
  "supported-services": [
    {
      "uid": "97aeb3d9-9aea-11d5-bd16-0090272ccb30",
      "name": "smtp",
      "type": "service-tcp",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      },
      "icon": "Protocols/MailProtocolEnvelope",
      "color": "magenta",
      "port": "25"
    },
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
      "uid": "704fbf04-1714-49a1-a750-38c0e4139a11",
      "name": "HTTPS_proxy",
      "type": "service-tcp",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      },
      "icon": "Protocols/HTTP",
      "color": "navy blue",
      "port": "8080"
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
    }
  ],
  "httpi-non-standard-ports": false,
  "inspect-archives": false
}
```
