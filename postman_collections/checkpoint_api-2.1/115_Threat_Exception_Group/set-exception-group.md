# set-exception-group

**Collection:** Web API (version 2.1) > 115 Threat Exception Group
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-exception-group`

## Description

Set exception group

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "exception_group_2",
  "new-name": "exception_group_2.1",
  "tags": "tag3"
}
```

## Example Responses

### Example 1: set-exception-group
**Status:** `200 OK`
