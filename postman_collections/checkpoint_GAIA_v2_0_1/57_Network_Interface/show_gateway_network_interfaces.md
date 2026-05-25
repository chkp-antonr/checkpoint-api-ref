# show gateway network interfaces

**Collection:** Web API (version 2.0.1) > 57 Network Interface
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-interfaces`

## Description

Show all network interfaces of a gateway.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "gateway-uid": "ff918e85-98c4-4b17-bcac-417aab863d87",
  "details-level": "full",
  "offset": 0,
  "limit": 50
}
```

## Example Responses

### Example 1: show gateway network interfaces
**Status:** `200 OK`
