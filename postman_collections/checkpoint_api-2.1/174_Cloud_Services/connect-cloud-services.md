# connect-cloud-services

**Collection:** Web API (version 2.1) > 174 Cloud Services
**Method:** `POST`
**URL:** `{{server}}/v2.1/connect-cloud-services`

## Description

Connect the management server to Check Point Smart-1 Cloud services.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "auth-token": "aHR0cHM6Ly9kZXYtY2xvdWRpbmZyYS1ndy5rdWJlMS5pYWFzLmNoZWNrcG9pbnQuY29tL2FwcC9tYWFzL2FwaS92Mi9tYW5hZ2VtZW50cy9hZmJlYWRlYS04Y2U2LTRlYTUtOTI4OS00ZTQ0N2M0ZjgyMTMvY2xvdWRBY2Nlc3MvP290cD02ZWIzNThlOS1hMzkxLTQxOGQtYjlmZi0xOGIxOTQwOGJlN2Y="
}
```

## Example Responses

### Example 1: connect-cloud-services
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
    "enabled": false,
    "participant-gateways": "all",
    "connection-method": "automatically",
    "specific-gateways": []
  },
  "tenant-id": "e2ff2164-e068-407a-a1c2-25864cdb431e",
  "environment-id": "e8772cdf-303e-4e58-9afe-2390cae717c0"
}
```
