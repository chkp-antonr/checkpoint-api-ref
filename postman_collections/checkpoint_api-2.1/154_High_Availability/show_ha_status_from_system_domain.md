# show ha status from system domain

**Collection:** Web API (version 2.1) > 154 High Availability
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-ha-status`

## Description

Shows HA sync status called from system domain.

## Request Headers

| Header | Value |
|--------|-------|
| Content-type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{}
```

## Example Responses

### Example 1: show ha status from system domain
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "a0eebc99-afed-4ef8-bb6d-fedfedfedfed",
  "name": "System Data",
  "domain-type": "mds",
  "successfully-synced": true
}
```
