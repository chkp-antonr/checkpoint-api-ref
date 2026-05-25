# set-network

**Collection:** Web API (version 2.1) > 06 Network
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-network`

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
  "new-name": "New Network 2",
  "color": "green",
  "subnet": "192.0.0.0",
  "mask-length": 16,
  "groups": "New Group 1"
}
```

## Example Responses

### Example 1: set-network
**Status:** `200 OK`
