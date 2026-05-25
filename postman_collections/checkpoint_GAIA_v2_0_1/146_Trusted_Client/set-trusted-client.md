# set-trusted-client

**Collection:** Web API (version 2.0.1) > 146 Trusted Client
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-trusted-client`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "my client",
  "type": "NETMASK",
  "ip-address": "192.0.2.1",
  "mask-length": "24"
}
```

## Example Responses

### Example 1: set-trusted-client
**Status:** `200 OK`
