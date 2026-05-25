# set-cloud-services

**Collection:** Web API (version 2.1) > 174 Cloud Services
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-cloud-services`

## Description

Edit the Gateways On-boarding settings.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "gateways-onboarding-settings": {
    "enabled": "true",
    "connection-method": "after install policy",
    "participant-gateways": "specific",
    "specific-gateways": "gw1"
  }
}
```

## Example Responses

### Example 1: set-cloud-services
**Status:** `200 OK`

**Body:**
```javascript
{
  "status": "connected",
  "connected-at": {
    "posix": 1638897548267,
    "iso-8601": "2021-12-07T19:19+0200"
  },
  "management-url": "https://web-server/app/maas/api/v2/environments/e8772cdf-303e-4e58-9afe-2390cae717c0",
  "gateways-onboarding-settings": {
    "enabled": true,
    "participant-gateways": "specific",
    "connection-method": "after install policy",
    "specific-gateways": [
      {
        "uid": "e4b448ef-2635-40f0-ac46-11751597c6c6",
        "name": "gw1",
        "type": "simple-gateway",
        "domain": {
          "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
          "name": "SMC User",
          "domain-type": "domain"
        },
        "icon": "NetworkObjects/gateway",
        "color": "black"
      }
    ]
  },
  "tenant-id": "e2ff2164-e068-407a-a1c2-25864cdb431e",
  "environment-id": "e8772cdf-303e-4e58-9afe-2390cae717c0"
}
```
