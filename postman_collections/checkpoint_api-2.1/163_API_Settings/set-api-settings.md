# set-api-settings

**Collection:** Web API (version 2.1) > 163 API Settings
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-api-settings`

## Description

Set API Settings

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "accepted-api-calls-from": "All IP addresses"
}
```

## Example Responses

### Example 1: set-api-settings
**Status:** `200 OK`
