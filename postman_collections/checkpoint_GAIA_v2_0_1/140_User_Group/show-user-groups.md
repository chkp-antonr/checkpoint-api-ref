# show-user-groups

**Collection:** Web API (version 2.0.1) > 140 User Group
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-user-groups`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "details-level": "full"
}
```

## Example Responses

### Example 1: show-user-groups
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 1,
  "total": 1,
  "objects": [
    {
      "uid": "8c7eb5af-0a27-43f8-a83c-bc38e900e75c",
      "name": "myusergroup",
      "type": "user-group",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "Objects/UsersGroup",
      "color": "black"
    }
  ]
}
```
