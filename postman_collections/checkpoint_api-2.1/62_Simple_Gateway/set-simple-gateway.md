# set-simple-gateway

**Collection:** Web API (version 2.1) > 62 Simple Gateway
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-simple-gateway`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "test_gateway",
  "vpn": true,
  "application-control": true,
  "url-filtering": true,
  "ips": true,
  "anti-bot": true,
  "anti-virus": true,
  "threat-emulation": true,
  "nat-hide-internal-interfaces": true,
  "icap-server": true
}
```

## Example Responses

### Example 1: set-simple-gateway
**Status:** `200 OK`
