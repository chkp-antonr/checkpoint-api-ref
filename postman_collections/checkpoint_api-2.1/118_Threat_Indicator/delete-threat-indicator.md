# delete-threat-indicator

**Collection:** Web API (version 2.1) > 118 Threat Indicator
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-threat-indicator`

## Description

Deleting a threat indicator

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "My_Indicator"
}
```

## Example Responses

### Example 1: delete-threat-indicator
**Status:** `200 OK`
