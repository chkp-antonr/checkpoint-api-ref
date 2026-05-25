# clone-host

**Collection:** Web API (version 2.1) > 05 Host
**Method:** `POST`
**URL:** `{{server}}/v2.1/clone-host`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Host 1",
  "ipv4-address": "192.0.2.2",
  "color": "green"
}
```

## Example Responses

### Example 1: clone-host
**Status:** `200 OK`
