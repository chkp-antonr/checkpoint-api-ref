# show-network-feeds

**Collection:** Web API (version 2.1) > 23 Network Feed
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-network-feeds`

## Description

Showing a list of Network Feeds

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{}
```

## Example Responses

### Example 1: show-network-feeds
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 1,
  "total": 1,
  "objects": [
    {
      "uid": "a1d2454c-d3cb-439e-9b29-c447b1cafd48",
      "name": "network_feed",
      "type": "network-feed",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      },
      "icon": "General/globalsNa",
      "color": "black"
    }
  ]
}
```
