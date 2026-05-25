# show the current attached licenses

**Collection:** Web API (version 2.1) > 189 Licenses
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-cloud-licenses-usage`

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

### Example 1: show the current attached licenses
**Status:** `200 OK`

**Body:**
```javascript
{
  "licenses-usage": [
    {
      "pool": "VE-FIREWALL",
      "cks": [
        "AAAAAAAA",
        "BBBBBBBB"
      ],
      "is-default": true,
      "total-quota": "37",
      "available-quota": "33",
      "subscribed-gateways": [
        {
          "name": "GW_A",
          "used-quota": "4"
        }
      ]
    }
  ]
}
```
