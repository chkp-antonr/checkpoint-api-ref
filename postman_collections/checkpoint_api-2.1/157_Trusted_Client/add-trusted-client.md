# add-trusted-client

**Collection:** Web API (version 2.1) > 157 Trusted Client
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-trusted-client`

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
  "type": "ANY"
}
```

## Example Responses

### Example 1: add-trusted-client
**Status:** `200 OK`
