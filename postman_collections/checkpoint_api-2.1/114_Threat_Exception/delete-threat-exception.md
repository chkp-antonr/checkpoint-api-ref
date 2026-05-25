# delete-threat-exception

**Collection:** Web API (version 2.1) > 114 Threat Exception
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-threat-exception`

## Description

Delete threat exception

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "rule-number": 1,
  "exception-number": 1,
  "layer": "New Layer 1"
}
```

## Example Responses

### Example 1: delete-threat-exception
**Status:** `200 OK`
