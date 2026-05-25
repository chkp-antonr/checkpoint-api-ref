# add-smart-task that sends an email after submit

**Collection:** Web API (version 2.1) > 143 SmartTasks
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-smart-task`

## Description

Adds a SmartTask that will run after submit and send an email notifying the recipients of the submitted session with a change report attached.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "Send Mail After Submit",
  "trigger": "After Submit",
  "description": "Notifying via email about a submitted session with change report attached.",
  "action": {
    "send-mail": {
      "mail-settings": {
        "subject": "A session was submitted",
        "recipients": "recipient1@example.com,recipient2@example.com",
        "sender-email": "sender@example.com",
        "body": "Please review my session",
        "attachment": "changes_report"
      },
      "smtp-server": "SMTP"
    }
  },
  "enabled": true
}
```

## Example Responses

### Example 1: add-smart-task that sends an email after submit
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "1baf4730-6a19-424c-8f6f-93393a956b8a",
  "name": "Send Mail After Submit",
  "type": "smart-task",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1639665028017,
      "iso-8601": "2021-12-16T16:30+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1639665028017,
      "iso-8601": "2021-12-16T16:30+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/SmartTask",
  "enabled": true,
  "trigger": {
    "uid": "4154075c-900f-40fa-8bf7-21dbf8421c44",
    "name": "After Submit",
    "type": "smart-task-trigger",
    "domain": {
      "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
      "name": "Check Point Data",
      "domain-type": "data domain"
    },
    "icon": "General/globalsNa",
    "color": "black"
  },
  "description": "Notifying via email about a submitted session with change report attached.",
  "fail-open": true,
  "custom-data": "",
  "action": {
    "send-mail": {
      "smtp-server": {
        "uid": "26b91119-43b0-4fd5-8db0-ac051319962c",
        "name": "SMTP",
        "type": "smtp-server",
        "domain": {
          "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
          "name": "SMC User",
          "domain-type": "domain"
        },
        "meta-info": {
          "lock": "locked by current session",
          "validation-state": "ok",
          "last-modify-time": {
            "posix": 1639472230980,
            "iso-8601": "2021-12-14T10:57+0200"
          },
          "last-modifier": "aa",
          "creation-time": {
            "posix": 1639472230980,
            "iso-8601": "2021-12-14T10:57+0200"
          },
          "creator": "aa"
        },
        "tags": [],
        "read-only": false,
        "comments": "",
        "color": "black",
        "icon": "Objects/account_unit",
        "server": "smtp.checkpoint.com",
        "port": 25,
        "username": ""
      },
      "mail-settings": {
        "subject": "A session was submitted",
        "recipients": "recipient1@example.com,recipient2@example.com",
        "body": "Please review my session",
        "sender-email": "sender@example.com",
        "attachment": "changes report"
      }
    }
  }
}
```
