# get attachment by log-id

**Collection:** Web API (version 2.1) > 173 Logs
**Method:** `POST`
**URL:** `{{server}}/v2.1/get-attachment`

## Description

Request for packet capture or blob data by log id.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "id": "ac17545e-eb6a-0000-5e4c-f4f700000000"
}
```

## Example Responses

### Example 1: get attachment by log-id
**Status:** `200 OK`
