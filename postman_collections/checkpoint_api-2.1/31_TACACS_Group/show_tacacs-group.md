# show tacacs-group

**Collection:** Web API (version 2.1) > 31 TACACS Group
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-tacacs-group`

## Description

Show tacacs group

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "group1"
}
```

## Example Responses

### Example 1: show tacacs-group
**Status:** `200 OK`
