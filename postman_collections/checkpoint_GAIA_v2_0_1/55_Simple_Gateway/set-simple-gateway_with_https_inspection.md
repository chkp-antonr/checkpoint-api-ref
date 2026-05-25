# set-simple-gateway with https inspection

**Collection:** Web API (version 2.0.1) > 55 Simple Gateway
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-simple-gateway`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "gw1",
  "https-inspection": {
    "bypass-on-failure": {
      "override-profile": "true",
      "value": "true"
    },
    "site-categorization-allow-mode": {
      "override-profile": "true",
      "value": "background"
    },
    "deny-untrusted-server-cert": {
      "override-profile": "true",
      "value": "true"
    },
    "deny-revoked-server-cert": {
      "override-profile": "true",
      "value": "true"
    },
    "deny-expired-server-cert": {
      "override-profile": "true",
      "value": "true"
    }
  }
}
```

## Example Responses

### Example 1: set-simple-gateway with https inspection
**Status:** `200 OK`
