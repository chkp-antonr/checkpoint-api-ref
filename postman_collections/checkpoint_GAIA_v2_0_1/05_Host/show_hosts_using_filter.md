# show hosts using filter

**Collection:** Web API (version 2.0.1) > 05 Host
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-hosts`

## Description

Show hosts using filter.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "filter": "host_"
}
```

## Example Responses

### Example 1: show hosts using filter
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 2,
  "total": 2,
  "objects": [
    {
      "uid": "6b6bf76d-9f9e-4655-bd2f-ca2db753fb94",
      "name": "host_1",
      "type": "host",
      "domain": {
        "uid": "a59b701f-79dd-49dd-b054-f3c92af4b608",
        "name": "dom82",
        "domain-type": "domain"
      },
      "icon": "Objects/host",
      "color": "cyan",
      "ipv4-address": "88.5.9.77"
    },
    {
      "uid": "94a3f624-48f2-4630-97cd-4468c7ca5af8",
      "name": "host_2",
      "type": "host",
      "domain": {
        "uid": "a59b701f-79dd-49dd-b054-f3c92af4b608",
        "name": "dom82",
        "domain-type": "domain"
      },
      "icon": "Objects/host",
      "color": "black",
      "ipv4-address": "43.77.34.4"
    }
  ]
}
```
