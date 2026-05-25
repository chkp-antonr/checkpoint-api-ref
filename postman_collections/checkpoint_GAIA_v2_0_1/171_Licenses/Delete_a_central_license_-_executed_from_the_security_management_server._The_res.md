# Delete a central license - executed from the security management server. The response is a list containing the remaining attached central licenses on the remote target.

**Collection:** Web API (version 2.0.1) > 171 Licenses
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/delete-central-license`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "signature": "dTTTTTT-WWWWWW-SSSSSSS-QQQQQQ"
}
```

## Example Responses

### Example 1: Delete a central license - executed from the security management server. The response is a list containing the remaining attached central licenses on the remote target.
**Status:** `200 OK`

**Body:**
```javascript
{
  "licenses": [
    {
      "ip-address": "192.168.1.1",
      "expiration": "never",
      "signature": "dLLLLL-WWWWWW-ZZZZZZ-QQQQQQ",
      "sku": "CPSG-VE+37 CPSB-BASE CPSB-FW CPSB-ADNC CPSB-SSLVPN-U CPSB-IPS-S1 CPSB-CTNT",
      "ck": "777773333",
      "central": true,
      "additional-info": {
        "type": "cloud",
        "pool": "VE-FIREWALL",
        "quota-value": "37",
        "quota-unit": "cores"
      }
    },
    {
      "ip-address": "192.168.1.1",
      "expiration": "2023-04-25",
      "signature": "dTIIIIII-RRRRRR-SSSSSSS-PPPPPP",
      "sku": "CPSB-BASE CPSB-FW CPSM-C-2 CPSB-VPN",
      "ck": "CHECK-POINT-INTERNAL-USE-ONLY",
      "central": true
    }
  ]
}
```
