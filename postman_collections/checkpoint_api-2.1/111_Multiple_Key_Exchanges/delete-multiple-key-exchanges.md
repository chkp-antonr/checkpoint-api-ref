# delete-multiple-key-exchanges

**Collection:** Web API (version 2.1) > 111 Multiple Key Exchanges
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-multiple-key-exchanges`

## Description

Delete an existing Multiple Key Exchanges.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "Multiple Key Exchanges"
}
```

## Example Responses

### Example 1: delete-multiple-key-exchanges
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
