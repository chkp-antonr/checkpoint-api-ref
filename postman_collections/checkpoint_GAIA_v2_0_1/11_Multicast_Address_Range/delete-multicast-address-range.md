# delete-multicast-address-range

**Collection:** Web API (version 2.0.1) > 11 Multicast Address Range
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/delete-multicast-address-range`

## Description

Deletes a Multicast Address Range

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Multicast Address Range"
}
```

## Example Responses

### Example 1: delete-multicast-address-range
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
