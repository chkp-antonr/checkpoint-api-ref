# delete-data-center-query

**Collection:** Web API (version 2.0.1) > 64 Data Center Query
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/delete-data-center-query`

## Description

Delete data center query

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "data-center-query1"
}
```

## Example Responses

### Example 1: delete-data-center-query
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
