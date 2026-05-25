# add-trusted-client with type "ipv4 address range"

**Collection:** Web API (version 2.0.1) > 146 Trusted Client
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-trusted-client`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "myclient",
  "type": "ipv4 address range",
  "ip-address-first": "1.2.3.4",
  "ip-address-last": "1.2.3.5"
}
```

## Example Responses

### Example 1: add-trusted-client with type "ipv4 address range"
**Status:** `200 OK`
