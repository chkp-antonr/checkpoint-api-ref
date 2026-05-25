# Add a central license - executed from the security management server

**Collection:** Web API (version 2.1) > 189 Licenses
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-central-license`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "license": "192.168.1.2 never dTTTTTT-WWWWWW-SSSSSSS-QQQQQQ CPSG-VE+3 CPBS-BECE CPSB-DFW CPSM-C-2 CPSB-VPN CPSB-NPM CPSB-LOGS CPSB-IA CPSB-ADNC CPSB-SSLVWPN-5 CK-66666666"
}
```

## Example Responses

### Example 1: Add a central license - executed from the security management server
**Status:** `200 OK`

**Body:**
```javascript
{
  "ck": "CK-66666666",
  "sku": "CPSG-VE+3 CPBS-BECE CPSB-DFW CPSM-C-2 CPSB-VPN CPSB-NPM CPSB-LOGS CPSB-IA CPSB-ADNC CPSB-SSLVWPN-5",
  "central": true,
  "expiration": "never",
  "ip-address": "192.168.1.2",
  "signature": "dTTTTTT-WWWWWW-SSSSSSS-QQQQQQ",
  "additional-info": {
    "type": "cloud",
    "pool": "VE-NGTP",
    "quota-value": "3",
    "quota-unit": "cores"
  }
}
```
