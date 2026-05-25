# show-app-control-advanced-settings In Global Domain

**Collection:** Web API (version 2.1) > 187 Application Ctrl & URL Filtering Advanced Settings
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-app-control-advanced-settings`

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

### Example 1: show-app-control-advanced-settings In Global Domain
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "4d009bbb-287b-4691-a04b-d027abd7793a",
  "type": "app-control-advanced-settings",
  "domain": {
    "uid": "1e294ce0-367a-11e3-aa6e-0800200c9a66",
    "name": "Global",
    "domain-type": "global domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1678796199681,
      "iso-8601": "2023-03-14T14:16+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1675751239124,
      "iso-8601": "2023-02-07T08:27+0200"
    },
    "creator": "System"
  },
  "available-actions": {
    "edit": "true",
    "delete": "true",
    "clone": "true"
  },
  "read-only": false,
  "web-browsing-services": [
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
      "uid": "97aeb44f-9aea-11d5-bd16-0090272ccb30",
      "name": "AOL",
      "type": "service-tcp",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      },
      "icon": "Services/TCPService",
      "color": "red",
      "port": "5190"
    }
  ],
  "match-application-on-any-port": true,
  "domain-level-permission": true
}
```
