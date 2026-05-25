# delete-network-probe

**Collection:** Web API (version 2.0.1) > 99 Network Probe
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/delete-network-probe`

## Description

Delete existing Network Probe using object name or uid.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "probe_GW1"
}
```

## Example Responses

### Example 1: delete-network-probe
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
