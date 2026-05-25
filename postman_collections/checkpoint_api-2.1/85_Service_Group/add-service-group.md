# add-service-group

**Collection:** Web API (version 2.1) > 85 Service Group
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-service-group`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Service Group 1",
  "members": [
    "https",
    "bootp",
    "nisplus",
    "HP-OpCdistm"
  ]
}
```

## Example Responses

### Example 1: add-service-group
**Status:** `200 OK`
