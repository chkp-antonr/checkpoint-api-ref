# Show the current given central license

**Collection:** Web API (version 2.1) > 189 Licenses
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-central-license`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "signature": "dLLLLL-WWWWWW-ZZZZZZ-QQQQQQ"
}
```

## Example Responses

### Example 1: Show the current given central license
**Status:** `200 OK`

**Body:**
```javascript
{
  "ck": "CK-777773333",
  "sku": "CPSG-VE+3 CPBS-BECE CPSB-DFW CPSM-C-2 CPSB-VPN CPSB-NPM CPSB-LOGS CPSB-IA CPSB-ADNC CPSB-SSLVWPN-5",
  "central": "true",
  "expiration": "2024-04-25",
  "ip-address": "192.168.1.1",
  "signature": "dLLLLL-WWWWWW-ZZZZZZ-QQQQQQ",
  "additional-info": {
    "type": "cloud",
    "pool": "FIREWALL",
    "quota-value": "3",
    "quota-unit": "cores"
  }
}
```
