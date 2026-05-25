# show-user-group

**Collection:** Web API (version 2.1) > 151 User Group
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-user-group`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "myusergroup"
}
```

## Example Responses

### Example 1: show-user-group
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "8c7eb5af-0a27-43f8-a83c-bc38e900e75c",
  "name": "myusergroup",
  "type": "user-group",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "locked by current session",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1640537839398,
      "iso-8601": "2021-12-26T18:57+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1640537839398,
      "iso-8601": "2021-12-26T18:57+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "Objects/UsersGroup",
  "groups": [],
  "email": "myusergroup@email.com",
  "members": []
}
```
