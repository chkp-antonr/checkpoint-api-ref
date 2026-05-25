# show ha status from local domain

**Collection:** Web API (version 2.0.1) > 143 High Availability
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-ha-status`

## Description

Shows HA sync status called from local active domain.

## Request Headers

| Header | Value |
|--------|-------|
| Content-type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{}
```

## Example Responses

### Example 1: show ha status from local domain
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "041ca0c2-c15f-4a70-8116-02933383bffb",
  "name": "domain1",
  "domain-type": "domain",
  "servers": [
    {
      "ip-address": "172.23.3.234",
      "ha-state": "standby",
      "multi-domain-server": "secondary",
      "last-successful-sync": {
        "posix": 1672146619056,
        "iso-8601": "2022-12-27T15:10+0200"
      },
      "sync-state": "Ok"
    },
    {
      "ip-address": "172.23.3.235",
      "ha-state": "standby",
      "multi-domain-server": "secondary2",
      "sync-state": "Sync Error"
    }
  ],
  "successfully-synced": false
}
```
