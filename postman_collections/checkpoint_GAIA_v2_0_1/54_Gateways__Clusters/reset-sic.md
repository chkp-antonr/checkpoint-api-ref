# reset-sic

**Collection:** Web API (version 2.0.1) > 54 Gateways & Clusters
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/reset-sic`

## Description

Reset SIC of gateway

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "gw1"
}
```

## Example Responses

### Example 1: reset-sic
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
