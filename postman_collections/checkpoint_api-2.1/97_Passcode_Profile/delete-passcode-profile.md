# delete-passcode-profile

**Collection:** Web API (version 2.1) > 97 Passcode Profile
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-passcode-profile`

## Description

Deleting a Passcode profile

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "My App Passcode Policy"
}
```

## Example Responses

### Example 1: delete-passcode-profile
**Status:** `200 OK`
