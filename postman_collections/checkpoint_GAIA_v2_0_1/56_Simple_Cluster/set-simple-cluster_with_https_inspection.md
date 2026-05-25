# set-simple-cluster with https inspection

**Collection:** Web API (version 2.0.1) > 56 Simple Cluster
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-simple-cluster`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "cluster1",
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
    "deny-expired-server-cer": {
      "override-profile": "true",
      "value": "true"
    }
  }
}
```

## Example Responses

### Example 1: set-simple-cluster with https inspection
**Status:** `200 OK`
