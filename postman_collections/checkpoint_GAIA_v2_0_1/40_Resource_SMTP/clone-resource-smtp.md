# clone-resource-smtp

**Collection:** Web API (version 2.0.1) > 40 Resource SMTP
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/clone-resource-smtp`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "apismtp"
}
```

## Example Responses

### Example 1: clone-resource-smtp
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "aead66ea-56e6-4d48-ab64-1d4a4614b19b",
  "name": "apismtp_Clone",
  "type": "resource-smtp",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1661350901835,
      "iso-8601": "2022-08-24T17:21+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1661350901835,
      "iso-8601": "2022-08-24T17:21+0300"
    },
    "creator": "aa"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Services/Resource",
  "mail-delivery-server": "",
  "deliver-messages-using-dns-mx-records": false,
  "check-rulebase-with-new-destination": false,
  "notify-sender-on-error": false,
  "error-mail-delivery-server": "",
  "error-deliver-messages-using-dns-mx-records": false,
  "error-check-rulebase-with-new-destination": false,
  "exception-track": {
    "uid": "97aeb47d-9aea-11d5-bd16-0090272ccb30",
    "name": "None",
    "type": "CpmiEmptyTrack",
    "domain": {
      "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
      "name": "Check Point Data",
      "domain-type": "data domain"
    },
    "icon": "Track/tracksLog"
  },
  "match": {},
  "cvp": {
    "enable-cvp": false,
    "cvp-server-is-allowed-to-modify-content": true,
    "reply-order": "return_data_after_content_is_approved"
  },
  "action-1": {
    "sender": {},
    "recipient": {},
    "custom-field": {}
  },
  "action-2": {
    "mail-capacity": 10000000,
    "allowed-characters": "8_bit"
  }
}
```
