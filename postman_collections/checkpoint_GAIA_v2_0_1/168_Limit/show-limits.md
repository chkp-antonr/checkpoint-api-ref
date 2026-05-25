# show-limits

**Collection:** Web API (version 2.0.1) > 168 Limit
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-limits`

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

### Example 1: show-limits
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 6,
  "total": 6,
  "objects": [
    {
      "uid": "eb891a4d-893c-42e9-b7db-20507fb45e09",
      "name": "Download_10Mbps",
      "type": "limit",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      },
      "icon": "Objects/limit",
      "color": "black"
    },
    {
      "uid": "04e6a535-0541-4139-b18f-abd47fa23598",
      "name": "Download_1Gbps",
      "type": "limit",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      },
      "icon": "Objects/limit",
      "color": "black"
    },
    {
      "uid": "769f6211-c8dc-4e79-8fe4-3842e5031c22",
      "name": "limit_obj",
      "type": "limit",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "Objects/limit",
      "color": "black"
    },
    {
      "uid": "85d46c45-5c87-4d7a-a686-84d1be3d1482",
      "name": "limit_obj_Clone",
      "type": "limit",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "Objects/limit",
      "color": "black"
    },
    {
      "uid": "42fef827-159b-4137-bf5e-34e851f1d1c1",
      "name": "Upload_10Mbps",
      "type": "limit",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      },
      "icon": "Objects/limit",
      "color": "black"
    },
    {
      "uid": "c1a949e2-3cf2-47f4-92a1-c9a4bb3e8144",
      "name": "Upload_1Gbps",
      "type": "limit",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      },
      "icon": "Objects/limit",
      "color": "black"
    }
  ]
}
```
