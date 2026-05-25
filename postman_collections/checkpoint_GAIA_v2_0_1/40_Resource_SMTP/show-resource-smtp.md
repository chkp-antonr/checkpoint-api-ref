# show-resource-smtp

**Collection:** Web API (version 2.0.1) > 40 Resource SMTP
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-resource-smtp`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "newSmtpResource"
}
```

## Example Responses

### Example 1: show-resource-smtp
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "a757ef84-02b2-4c09-85c0-333aeb761ea9",
  "name": "newSmtpResource",
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
      "posix": 1661256955264,
      "iso-8601": "2022-08-23T15:15+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1661243010930,
      "iso-8601": "2022-08-23T11:23+0300"
    },
    "creator": "aa"
  },
  "available-actions": {
    "edit": "true",
    "delete": "true",
    "clone": "true"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "Services/Resource",
  "mail-delivery-server": "newServer",
  "deliver-messages-using-dns-mx-records": true,
  "check-rulebase-with-new-destination": false,
  "notify-sender-on-error": false,
  "error-mail-delivery-server": "",
  "error-deliver-messages-using-dns-mx-records": false,
  "error-check-rulebase-with-new-destination": false,
  "exception-track": {
    "uid": "97aeb48d-9aea-11d5-bd16-0090272ccb30",
    "name": "Exception Log",
    "type": "CpmiLog",
    "domain": {
      "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
      "name": "Check Point Data",
      "domain-type": "data domain"
    },
    "icon": "Track/tracksLog",
    "color": "blue"
  },
  "match": {
    "sender": "senderName",
    "recipient": "recipientName"
  },
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
    "mail-capacity": 10000,
    "allowed-characters": "8_bit"
  }
}
```
