# add-network

**Collection:** Web API (version 2.1) > 06 Network
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-network`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Network 1",
  "subnet": "192.0.2.0",
  "subnet-mask": "255.255.255.0"
}
```

## Example Responses

### Example 1: add-network
**Status:** `200 OK`
