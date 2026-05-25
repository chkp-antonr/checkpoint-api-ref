# Update Provisioned Satellites

**Collection:** Web API (version 2.1) > 176 Provisioning
**Method:** `POST`
**URL:** `{{server}}/v2.1/update-provisioned-satellites`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "vpn-center-gateways": [
    "co_gateway"
  ]
}
```

## Example Responses

### Example 1: Update Provisioned Satellites
**Status:** `200 OK`
