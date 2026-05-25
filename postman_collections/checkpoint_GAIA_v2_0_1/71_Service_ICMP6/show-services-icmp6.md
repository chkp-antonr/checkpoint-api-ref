# show-services-icmp6

**Collection:** Web API (version 2.0.1) > 71 Service ICMP6
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-services-icmp6`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "limit": 2,
  "offset": 4
}
```

## Example Responses

### Example 1: show-services-icmp6
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 5,
  "to": 6,
  "total": 25,
  "objects": [
    {
      "uid": "6f23dae7-0b9a-44f6-8515-b24690cd996c",
      "name": "home-agent-address-discovery2",
      "type": "service-icmp6",
      "domain": {
        "domain-type": "data domain",
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data"
      }
    },
    {
      "uid": "f645e71b-27cd-43ac-8512-619867ac0c79",
      "name": "ICMP-node-information-query",
      "type": "service-icmp6",
      "domain": {
        "domain-type": "data domain",
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data"
      }
    }
  ]
}
```
