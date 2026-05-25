# add-user-group

**Collection:** Web API (version 2.0.1) > 140 User Group
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-user-group`

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
  "email": "myusergroup@email.com",
  "members": "myuser"
}
```

## Example Responses

### Example 1: add-user-group
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "86f408cb-e1f7-44c9-838e-d988661e296f",
  "name": "myusergroup",
  "type": "user-group",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/UsersGroup",
  "groups": [],
  "email": "myusergroup@email.com",
  "members": [
    {
      "uid": "999ac8f2-196f-4e68-b282-8939cd5a5af3",
      "name": "myuser",
      "type": "user",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    }
  ]
}
```
