# set-user-group

**Collection:** Web API (version 2.0.1) > 140 User Group
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-user-group`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "myusergroup",
  "email": "myusergroup123@email.com",
  "new-name": "newusergroupname",
  "members": {
    "remove": [
      "myuser"
    ]
  }
}
```

## Example Responses

### Example 1: set-user-group
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "2bf9060c-a234-443c-943c-878ea501b6c9",
  "name": "newusergroupname",
  "type": "user-group",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "Objects/UsersGroup",
  "groups": [],
  "email": "myusergroup123@email.com",
  "members": []
}
```
