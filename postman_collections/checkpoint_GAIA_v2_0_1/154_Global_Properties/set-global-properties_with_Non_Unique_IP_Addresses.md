# set-global-properties with Non Unique IP Addresses

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
  "non-unique-ip-address-ranges": {
    "add": [
      {
        "address-type": "ipv4",
        "first-ipv4-address": "1.2.3.4",
        "last-ipv4-address": "5.6.7.8"
      },
      {
        "address-type": "ipv6",
        "first-ipv6-address": "2001:db8:85a3::8a2e:370:7334",
        "last-ipv6-address": "2001:db8:85a3::8a2e:370:7335"
      }
    ]
  }
}
```

## Example Responses

### Example 1: set-global-properties with Non Unique IP Addresses
**Status:** `200 OK`
