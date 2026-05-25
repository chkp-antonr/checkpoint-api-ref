# delete subordinate ca

**Collection:** Web API (version 2.1) > 45 Subordinate CA
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-subordinate-ca`

## Description

Delete existing subordinate CA.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "TestSubordinateCa"
}
```

## Example Responses

### Example 1: delete subordinate ca
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
