# set-simple-gateway with exported routes: custom routes

**Collection:** Web API (version 2.1) > 62 Simple Gateway
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-simple-gateway`

## Description

Sets a simple gateway with custom exported routes

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "GW_R8210_with_exported_routes",
  "vpn-settings": {
    "exported-routes": {
      "custom-routes": true,
      "custom-routes-object": "my_network"
    }
  }
}
```

## Example Responses

### Example 1: set-simple-gateway with exported routes: custom routes
**Status:** `200 OK`
