# set tacacs-group

**Collection:** Web API (version 2.0.1) > 25 TACACS Group
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-tacacs-group`

## Description

Set tacacs group

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "group1",
  "members": [
    "tacacs4"
  ]
}
```

## Example Responses

### Example 1: set tacacs-group
**Status:** `200 OK`
