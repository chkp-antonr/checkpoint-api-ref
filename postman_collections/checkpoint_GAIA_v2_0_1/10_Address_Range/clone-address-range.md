# clone-address-range

**Collection:** Web API (version 2.0.1) > 10 Address Range
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/clone-address-range`

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
  "new-name": "New Address Range 2",
  "color": "green",
  "ip-address-first": "192.0.2.1",
  "ip-address-last": "192.0.2.1",
  "groups": "New Group 1"
}
```

## Example Responses

### Example 1: clone-address-range
**Status:** `200 OK`
