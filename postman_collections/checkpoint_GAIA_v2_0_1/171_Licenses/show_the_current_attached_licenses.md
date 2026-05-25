# Show the current attached licenses

**Collection:** Web API (version 2.0.1) > 171 Licenses
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-central-licenses`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{}
```

## Example Responses

### Example 1: Show the current attached licenses
**Status:** `200 OK`

**Body:**
```javascript
{
  "licenses": [
    {
      "ck": "CK-777773333",
      "sku": "CPSG-VE+3 CPBS-BECE CPSB-DFW CPSM-C-2 CPSB-VPN CPSB-NPM CPSB-LOGS CPSB-IA CPSB-ADNC CPSB-SSLVWPN-5",
      "central": "true",
      "expiration": "never",
      "ip-address": "192.168.1.1",
      "signature": "dLLLLL-WWWWWW-ZZZZZZ-QQQQQQ",
      "additional-info": {
        "type": "cloud",
        "pool": "FIREWALL",
        "quota-value": "3",
        "quota-unit": "cores"
      }
    },
    {
      "CK": "CHECK-POINT-INTERNAL-USE-ONLY",
      "SKU": "CPSB-BASE CPSB-FW CPSM-C-2 CPSB-VPN",
      "central": "true",
      "expiration": "2023-04-25",
      "ip-address": "192.168.1.1",
      "signature": "dTIIIIII-RRRRRR-SSSSSSS-PPPPPP"
    }
  ]
}
```
