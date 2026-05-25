# delete tacacs-group

**Collection:** Web API (version 2.0.1) > 25 TACACS Group
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/delete-tacacs-group`

## Description

Delete an existing tacacs group

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "tacacs group"
}
```

## Example Responses

### Example 1: delete tacacs-group
**Status:** `200 OK`
