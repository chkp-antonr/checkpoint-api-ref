# set-global-properties with a new added HTTP Server

**Collection:** Web API (version 2.0.1) > 154 Global Properties
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-global-properties`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "firewall": {
    "security-server": {
      "http-servers": {
        "add": {
          "logical-name": "unique logical name",
          "host": "host name of server",
          "port": 8080,
          "reauthentication": "post request"
        }
      }
    }
  }
}
```

## Example Responses

### Example 1: set-global-properties with a new added HTTP Server
**Status:** `200 OK`
