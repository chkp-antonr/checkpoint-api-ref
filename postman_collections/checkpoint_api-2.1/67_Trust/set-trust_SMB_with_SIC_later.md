# set-trust SMB with SIC later

**Collection:** Web API (version 2.1) > 67 Trust
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-trust`

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
  "one-time-password": "aaaa",
  "trust-settings": {
    "initiation-phase": "when_gateway_connects"
  }
}
```

## Example Responses

### Example 1: set-trust SMB with SIC later
**Status:** `200 OK`
