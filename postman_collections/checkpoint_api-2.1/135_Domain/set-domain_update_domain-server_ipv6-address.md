# set-domain update domain-server ipv6-address

**Collection:** Web API (version 2.1) > 135 Domain
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-domain`

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
  "servers.update.ipv6-address": "2001:db8:85a3::8a2e:370:7329",
  "servers.update.name": "domain1_ManagementServer_1",
  "servers.update.multi-domain-server": "MDM_Server",
  "servers.update,restart-domain-server": "true"
}
```

## Example Responses

### Example 1: set-domain update domain-server ipv6-address
**Status:** `200 OK`
