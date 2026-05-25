# show-mdss

**Collection:** Web API (version 2.0.1) > 126 Multi-Domain Server (MDS)
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-mdss`

## Description

Show all the domains

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

### Example 1: show-mdss
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 1,
  "total": 1,
  "objects": [
    {
      "folder": {
        "uid": "a3a104fc-3987-4d22-9bf1-3fdbec0af39e",
        "name": "Global Objects"
      },
      "domain": {
        "domain-type": "system domain",
        "uid": "a0eebc99-afed-4ef8-bb6d-fedfedfedfed",
        "name": "System Data"
      },
      "type": "mds",
      "name": "test_mds",
      "uid": "d4ea2802-a148-48ac-8f21-fcce69588700"
    }
  ]
}
```
