# add tacacs-group

**Collection:** Web API (version 2.0.1) > 25 TACACS Group
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-tacacs-group`

## Description

Add tacacs group

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "group2",
  "members": [
    "t1",
    "t3",
    "group1"
  ]
}
```

## Example Responses

### Example 1: add tacacs-group
**Status:** `200 OK`
