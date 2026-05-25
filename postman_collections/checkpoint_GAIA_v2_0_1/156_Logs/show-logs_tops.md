# show-logs tops

**Collection:** Web API (version 2.0.1) > 156 Logs
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-logs`

## Description

Quering for tops.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "new-query": {
    "top": {
      "field": "blades",
      "count": "10"
    }
  }
}
```

## Example Responses

### Example 1: show-logs tops
**Status:** `200 OK`

**Body:**
```javascript
{
  "tops": [
    {
      "Firewall": "717"
    },
    {
      "System Monitor": "132"
    },
    {
      "HTTPS Inspection": "25"
    },
    {
      "Threat Emulation": "15"
    },
    {
      "Application Control": "14"
    },
    {
      "Identity Awareness": "7"
    },
    {
      "Mobile Access": "7"
    },
    {
      "URL Filtering": "7"
    },
    {
      "SmartEvent Client": "4"
    },
    {
      "SmartConsole": "2"
    }
  ],
  "query-id": "WEB_API_f942e748-e809-4308-ace7-2b3b1d5b72c1",
  "tops-count": "935"
}
```
