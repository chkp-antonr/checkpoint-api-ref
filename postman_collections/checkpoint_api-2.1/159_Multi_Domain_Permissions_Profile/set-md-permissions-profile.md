# set-md-permissions-profile

**Collection:** Web API (version 2.1) > 159 Multi Domain Permissions Profile
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-md-permissions-profile`

## Description

Change the default profile for all global domains in a Manager permission-level profile

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "manager profile",
  "permission-level": "domain level only",
  "default-profile-global-domains": "read write all"
}
```

## Example Responses

### Example 1: set-md-permissions-profile
**Status:** `200 OK`
