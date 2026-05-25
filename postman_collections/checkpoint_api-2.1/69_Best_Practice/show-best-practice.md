# show-best-practice

**Collection:** Web API (version 2.1) > 69 Best Practice
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-best-practice`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "best-practice-id": "FW183"
}
```

## Example Responses

### Example 1: show-best-practice
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "1fd4fdc9-3966-4880-a8fa-c1ec2a3b13f3",
  "name": "Check the Inspection settings: Non-TCP Flooding",
  "type": "compliance-best-practice",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1752526857500,
      "iso-8601": "2025-07-15T00:00+0300"
    },
    "last-modifier": "System",
    "creation-time": {
      "posix": 1752485587637,
      "iso-8601": "2025-07-14T12:33+0300"
    },
    "creator": "System"
  },
  "available-actions": {
    "edit": "true",
    "delete": "true",
    "clone": "true"
  },
  "read-only": false,
  "comments": "",
  "best-practice-id": "FW183",
  "description": "This checks the Inspection settings: Non-TCP Flooding to ensure that it is set to Drop and its Track setting is not set to 'None' on all relevant profiles",
  "action-item": "Inspection settings: Non-TCP Flooding must be set to Drop and its Track setting is not set to 'None' on all relevant profiles",
  "status": "poor",
  "blade": "firewall",
  "due-date": "",
  "user-defined": false,
  "relevant-objects": {
    "relevant-objects-type": "ips-protection",
    "ips-protections-info": [
      {
        "profile-uid": "1963f7ae-ea67-4826-ac48-e449bf5d2937",
        "protection-name": "Non-TCP Flooding",
        "profile-name": "Default Inspection",
        "action": "n_a",
        "status": "poor",
        "enabled": true
      }
    ]
  },
  "active": true
}
```
