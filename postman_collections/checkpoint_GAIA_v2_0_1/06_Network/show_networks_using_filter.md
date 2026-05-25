# show networks using filter

**Collection:** Web API (version 2.0.1) > 06 Network
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-networks`

## Description

Show networks using filter.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "filter": "network_"
}
```

## Example Responses

### Example 1: show networks using filter
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 2,
  "total": 2,
  "objects": [
    {
      "uid": "270deb32-072f-4d6d-892e-8e1e42c8edd8",
      "name": "network_1",
      "type": "network",
      "domain": {
        "uid": "a59b701f-79dd-49dd-b054-f3c92af4b608",
        "name": "dom82",
        "domain-type": "domain"
      },
      "icon": "NetworkObjects/network",
      "color": "black",
      "subnet4": "43.6.2.0",
      "subnet-mask": "255.255.255.0",
      "mask-length4": 24
    },
    {
      "uid": "1f8642b4-0fda-493d-885c-8b97305b4864",
      "name": "network_2",
      "type": "network",
      "domain": {
        "uid": "a59b701f-79dd-49dd-b054-f3c92af4b608",
        "name": "dom82",
        "domain-type": "domain"
      },
      "icon": "NetworkObjects/network",
      "color": "black",
      "subnet4": "34.5.21.0",
      "subnet-mask": "255.255.255.0",
      "mask-length4": 24
    }
  ]
}
```
