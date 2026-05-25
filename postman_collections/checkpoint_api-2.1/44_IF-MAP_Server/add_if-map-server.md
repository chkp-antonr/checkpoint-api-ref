# add if-map-server

**Collection:** Web API (version 2.1) > 44 IF-MAP Server
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-if-map-server`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "TestIfMapServer",
  "host": "TestHost",
  "version": "2.0",
  "port": 1,
  "path": "path",
  "monitored-ips": [
    {
      "first-ip": "1.1.1.1",
      "last-ip": "1.1.1.2"
    },
    {
      "first-ip": "2.1.1.1",
      "last-ip": "2.1.1.2"
    }
  ],
  "authentication": {
    "authentication-method": "certificate_based"
  }
}
```

## Example Responses

### Example 1: add if-map-server
**Status:** `200 OK`
