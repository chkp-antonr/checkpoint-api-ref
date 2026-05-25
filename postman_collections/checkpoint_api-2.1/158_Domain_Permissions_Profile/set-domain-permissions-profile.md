# set-domain-permissions-profile

**Collection:** Web API (version 2.1) > 158 Domain Permissions Profile
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-domain-permissions-profile`

## Description

Change permission-type and Access Control Policy Layers editing permissions

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "read profile",
  "new-name": "customized profile",
  "permission-type": "customized",
  "access-control.policy-layers": "By Selected Profile In A Layer Editor"
}
```

## Example Responses

### Example 1: set-domain-permissions-profile
**Status:** `200 OK`
