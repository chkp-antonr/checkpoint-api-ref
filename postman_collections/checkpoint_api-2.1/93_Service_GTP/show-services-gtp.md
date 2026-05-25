# show-services-gtp

**Collection:** Web API (version 2.1) > 93 Service GTP
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-services-gtp`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "limit": 10,
  "offset": 0,
  "details-level": "standard"
}
```

## Example Responses

### Example 1: show-services-gtp
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 10,
  "total": 13,
  "objects": [
    {
      "uid": "f9b8ae30-1d2f-4d76-a892-06d2e1b57fc1",
      "name": "gtp_additional_v2_default",
      "type": "service-gtp",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      }
    },
    {
      "uid": "b1834f14-743a-41fa-bdc5-0a3d85e1cbb6",
      "name": "gtp_mm_v0_default",
      "type": "service-gtp",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      }
    },
    {
      "uid": "51bfc325-c85e-4107-9cfc-d68a483d4f29",
      "name": "gtp_mm_v1_default",
      "type": "service-gtp",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      }
    },
    {
      "uid": "2e0fb7bd-e829-4ab3-9472-74af4120e472",
      "name": "gtp_mm_v2_default",
      "type": "service-gtp",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      }
    },
    {
      "uid": "d9531700-f8bb-4e3b-983d-10d69906a028",
      "name": "gtp_v0_default",
      "type": "service-gtp",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      }
    },
    {
      "uid": "aff26f18-b9b0-4e7c-bc4d-d6749e0487b2",
      "name": "gtp_v1_default",
      "type": "service-gtp",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      }
    },
    {
      "uid": "f2ff9d84-8cd5-414f-a9c6-0c00f937ee24",
      "name": "gtp_v2_default",
      "type": "service-gtp",
      "domain": {
        "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
        "name": "Check Point Data",
        "domain-type": "data domain"
      }
    },
    {
      "uid": "4ef4ed8e-9a7c-4eaf-9bcb-e30a77cd7820",
      "name": "New_gtp_Service_1",
      "type": "service-gtp",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    },
    {
      "uid": "f4816496-a806-46d1-94cd-38d83ec2526f",
      "name": "New_gtp_Service_2",
      "type": "service-gtp",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    },
    {
      "uid": "f19de81a-ad83-45d0-b98c-27d0a30a2fbd",
      "name": "New_gtp_Service_3",
      "type": "service-gtp",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    }
  ]
}
```
