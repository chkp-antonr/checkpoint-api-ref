# delete ldap-group

**Collection:** Web API (version 2.0.1) > 142 LDAP Group
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/delete-ldap-group`

## Description

Delete existing LDAP group.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "TestLdapGroup"
}
```

## Example Responses

### Example 1: delete ldap-group
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
