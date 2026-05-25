# add-address-range

**Collection:** Web API (version 2.1) > 10 Address Range
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-address-range`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Address Range 1",
  "ip-address-first": "192.0.2.1",
  "ip-address-last": "192.0.2.10"
}
```

## Example Responses

### Example 1: add-address-range
**Status:** `200 OK`
