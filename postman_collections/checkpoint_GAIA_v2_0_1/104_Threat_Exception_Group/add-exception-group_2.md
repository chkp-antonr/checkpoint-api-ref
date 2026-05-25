# add-exception-group

**Collection:** Web API (version 2.0.1) > 104 Threat Exception Group
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-exception-group`

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
  "apply-on": "manually-select-threat-rules",
  "applied-threat-rules.0.layer": "MyLayer",
  "applied-threat-rules.0.name": "MyThreatRule"
}
```

## Example Responses

### Example 1: add-exception-group
**Status:** `200 OK`
