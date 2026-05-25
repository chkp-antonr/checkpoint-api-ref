# show-data-center-queries

**Collection:** Web API (version 2.1) > 75 Data Center Query
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-data-center-queries`

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

### Example 1: show-data-center-queries
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 1,
  "total": 1,
  "objects": [
    {
      "uid": "4f50908f-4f45-4b70-87a3-2fbd87eca5f7",
      "name": "data-center-query1",
      "type": "data-center-query",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    }
  ]
}
```
