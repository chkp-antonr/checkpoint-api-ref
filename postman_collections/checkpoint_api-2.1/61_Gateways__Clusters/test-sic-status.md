# test-sic-status

**Collection:** Web API (version 2.1) > 61 Gateways & Clusters
**Method:** `POST`
**URL:** `{{server}}/v2.1/test-sic-status`

## Description

Test SIC status of gateway, output indicates state of the gateway which is communicating

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

### Example 1: test-sic-status
**Status:** `200 OK`

**Body:**
```javascript
{
  "sic-status:": "SIC Status for gw1: Communicating"
}
```
