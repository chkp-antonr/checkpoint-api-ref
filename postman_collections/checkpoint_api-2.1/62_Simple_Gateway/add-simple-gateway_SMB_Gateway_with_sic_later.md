# add-simple-gateway SMB Gateway with sic later

**Collection:** Web API (version 2.1) > 62 Simple Gateway
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-simple-gateway`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "smb_gw",
  "ipv4-address": "192.0.2.230",
  "one-time-password": "aaaa",
  "trust-settings": {
    "initiation-phase": "when_gateway_connects"
  }
}
```

## Example Responses

### Example 1: add-simple-gateway SMB Gateway with sic later
**Status:** `200 OK`
