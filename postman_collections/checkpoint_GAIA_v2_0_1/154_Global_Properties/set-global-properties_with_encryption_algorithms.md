# set-global-properties with encryption algorithms

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
  "remote-access": {
    "vpn-authentication-and-encryption": {
      "encryption-algorithms": {
        "ipsec": {
          "support-encryption-algorithms": {
            "tdes": true,
            "aes-256": true
          },
          "use-encryption-algorithm": "aes-256"
        }
      }
    }
  }
}
```

## Example Responses

### Example 1: set-global-properties with encryption algorithms
**Status:** `200 OK`
