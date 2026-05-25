# add-domain

**Collection:** Web API (version 2.0.1) > 124 Domain
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-domain`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "domain1",
  "servers": {
    "ip-address": "192.0.2.1",
    "name": "domain1_ManagementServer_1",
    "multi-domain-server": "MDM_Server"
  }
}
```

## Example Responses

### Example 1: add-domain
**Status:** `200 OK`
