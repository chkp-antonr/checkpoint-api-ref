# delete voip-domain-mgcp-call-agent

**Collection:** Web API (version 2.1) > 26 VoIP Domain MGCP Call Agent
**Method:** `POST`
**URL:** `{{server}}/v2.1/delete-voip-domain-mgcp-call-agent`

## Description

Delete existing voip domain mgcp call agent.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "mgcp1"
}
```

## Example Responses

### Example 1: delete voip-domain-mgcp-call-agent
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
