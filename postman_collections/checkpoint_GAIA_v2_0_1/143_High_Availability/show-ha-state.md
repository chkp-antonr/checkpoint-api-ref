# show-ha-state

**Collection:** Web API (version 2.0.1) > 143 High Availability
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-ha-state`

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

### Example 1: show-ha-state
**Status:** `200 OK`

**Body:**
```javascript
{
  "domains": [
    {
      "uid": "1e294ce0-367a-11e3-aa6e-0800200c9a66",
      "name": "Global",
      "domain-type": "global domain",
      "servers": [
        {
          "ip-address": "2.2.2.2",
          "ha-state": "standby",
          "multi-domain-server": "mds2"
        },
        {
          "ip-address": "1.1.1.1",
          "ha-state": "active",
          "multi-domain-server": "mds1"
        }
      ]
    },
    {
      "uid": "f23c1f26-210c-4222-b268-07b143dbba35",
      "name": "domain1",
      "domain-type": "domain",
      "servers": [
        {
          "name": "domain1_Server",
          "ip-address": "3.3.3.3",
          "ha-state": "active",
          "multi-domain-server": "mds1"
        },
        {
          "name": "domain1_Server_2",
          "ip-address": "4.4.4.4",
          "ha-state": "standby",
          "multi-domain-server": "mds2"
        }
      ]
    },
    {
      "uid": "7f4b2d3c-dd1d-40b0-a224-1a482fb28001",
      "name": "domain2",
      "domain-type": "domain",
      "servers": [
        {
          "name": "domain2_Server",
          "ip-address": "5.5.5.5",
          "ha-state": "active",
          "multi-domain-server": "mds1"
        },
        {
          "name": "domain2_Server_2",
          "ip-address": "6.6.6.6",
          "ha-state": "standby",
          "multi-domain-server": "mds2"
        }
      ]
    }
  ]
}
```
