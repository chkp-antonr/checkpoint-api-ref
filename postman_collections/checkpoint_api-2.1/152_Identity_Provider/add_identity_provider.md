# add identity provider

**Collection:** Web API (version 2.1) > 152 Identity Provider
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-identity-provider`

## Description

Create new identity provider.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "TestIdp2",
  "usage": "managing_administrator_access",
  "data-receiving": "manually",
  "received-identifier": "https://sts.checkpoint.net/621ac12d-4afb-479c-9c14-13e7b743cd07/",
  "login-url": "https://login.checkpointonline.com/621ac12d-4afb-479c-9c14-13e7b743cd07/saml2",
  "base64-certificate": "LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tCk1JSUM4RENDQWRpZ0F3SUJBZ0lRUTBWZVpLdVBLb0pQUWhaNGhDaWRzREFOQmdrcWhraUc5dzBCQVFzRkFEQTBNVEl3TUFZRFZRUURFeWxOYVdOeWIzTnZablFnUVhwMWNtVWdSbVZrWlhKaGRHVmtJRk5UVHlCRFpYSjBhV1pwWTJGMFpUQWVGdzB4T0RBME1UVXhNVEl6TXpOYUZ3MHlNVEEwTVRVeE1USXpNek5hTURReE1qQXdCZ05WQkFNVEtVMXBZM0p2YzI5bWRDQkJlblZ5WlNCR1pXUmxjbUYwWldRZ1UxTlBJRU5sY25ScFptbGpZWFJsTUlJQklqQU5CZ2txaGtpRzl3MEJBUUVGQUFPQ0FROEFNSUlCQ2dLQ0FRRUE0VXVqYUd0OFhaODl2dXZ5a3lRVzVYb24vOFIvaVB0ejRhYjBNM3RNVXZHWHozVXh0V1pTRStUR1hydjN3VHRLMCs4RmtNeXVKYUhGSXBLLzRVREZpRk1yQmxzR0Z1dmtTc1p5VjIzZlNGN3paaXlUWTZUN0EwcCtnczUwNVhEOUdBYjlWYmR3R0cwK0tDVnlpc1ZRZ1YySXdKZ2l5aHF3RUNvY3dCcmFuN251SytURU5EMmwyZjlZcng1b1JNRU56NzB3bHlIMzZPWkJtdDBrNTk4L1doMEhEWUxaZW8wZHlTV3JOd3dlWXZTeEU4L01kbTQzWEV1U3pialR6ZnNNMHZVUndGQlNyVUxFYURPMS9JUDJVcjdCc2dId1JJL3hmb3FJbUsxS2twVXEwQWxjVEFpM3YxdTl6Qy9xTGdQd0F5UUl2dzlVQ3NpcnJQQTBZMFlPaFFJREFRQUJNQTBHQ1NxR1NJYjNEUUVCQ3dVQUE0SUJBUURjam9qZEd6L0FJQ2pqTTBaN21ZbGdQNXpic2FRNWRDMmNqZjRESnFta21zV3VmUnBDNHNic3VoODcwY0NCS2N1dmgrb0dpekJRSHJQbTRUaEl2ZklsS0w4WGpMQVhiRnVSUG9IQWcwOHNMWGR2UFRCVE52REYxTWhvcU5zMmo2ZUZxL2ROdXF2ZUJIcjVENXRLblYyWEJHRUhFOVJFOVdUa1pRT2MwaEhtQ3dNbWNZb3JYRzhCa3l1OXFwNXhyMDZMQ0htMnJLcnI2ZENRVldBV0R0MzhiS2t5STRobTVSNTVCclR5UldSdzI1RS9YaFEwVksva1FJYW9GZ0hvaWo0ekg5bmxlZnZMbmhaZDVPRzROL29OS2pBKy9LbkVqaTdPQXhKWVNaR1FmRjU0R1AwQTE4VnF1NVVGaFBKMUZFQXZ5YjR0QnZtTzM1NFFVUys5UTY2agotLS0tLUVORCBDRVJUSUZJQ0FURS0tLS0t"
}
```

## Example Responses

### Example 1: add identity provider
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "a1f48d0f-d7e2-4302-85e1-6c89f77ad07d",
  "name": "TestIdp2",
  "type": "identity-provider",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1743420822840,
      "iso-8601": "2025-03-31T14:33+0300"
    },
    "last-modifier": "WEB_API",
    "creation-time": {
      "posix": 1743420822840,
      "iso-8601": "2025-03-31T14:33+0300"
    },
    "creator": "WEB_API"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/AuthenticationServer",
  "usage": "managing_administrator_access",
  "gateway": {
    "uid": "6c488338-8eec-4103-ad21-cd461ac2c471",
    "name": "None",
    "type": "Global",
    "domain": {
      "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
      "name": "Check Point Data",
      "domain-type": "data domain"
    },
    "icon": "General/globalsNone",
    "color": "none"
  },
  "service": "none",
  "required-identifier": "https://mgmt-sp-9af27867-672c-4c28-a4fe-900dfecb9f09.local/cpmws/saml/acs/id/9af27867-672c-4c28-a4fe-900dfecb9f09",
  "reply-urls": [
    "https://172.23.48.145/cpmws/saml/acs/sso"
  ],
  "data-receiving": "manually",
  "received-identifier": "https://sts.checkpoint.net/621ac12d-4afb-479c-9c14-13e7b743cd07/",
  "login-url": "https://login.checkpointonline.com/621ac12d-4afb-479c-9c14-13e7b743cd07/saml2",
  "base64-certificate": "LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tCk1JSUM4RENDQWRpZ0F3SUJBZ0lRUTBWZVpLdVBLb0pQUWhaNGhDaWRzREFOQmdrcWhraUc5dzBCQVFzRkFEQTBNVEl3TUFZRFZRUURFeWxOYVdOeWIzTnZablFnUVhwMWNtVWdSbVZrWlhKaGRHVmtJRk5UVHlCRFpYSjBhV1pwWTJGMFpUQWVGdzB4T0RBME1UVXhNVEl6TXpOYUZ3MHlNVEEwTVRVeE1USXpNek5hTURReE1qQXdCZ05WQkFNVEtVMXBZM0p2YzI5bWRDQkJlblZ5WlNCR1pXUmxjbUYwWldRZ1UxTlBJRU5sY25ScFptbGpZWFJsTUlJQklqQU5CZ2txaGtpRzl3MEJBUUVGQUFPQ0FROEFNSUlCQ2dLQ0FRRUE0VXVqYUd0OFhaODl2dXZ5a3lRVzVYb24vOFIvaVB0ejRhYjBNM3RNVXZHWHozVXh0V1pTRStUR1hydjN3VHRLMCs4RmtNeXVKYUhGSXBLLzRVREZpRk1yQmxzR0Z1dmtTc1p5VjIzZlNGN3paaXlUWTZUN0EwcCtnczUwNVhEOUdBYjlWYmR3R0cwK0tDVnlpc1ZRZ1YySXdKZ2l5aHF3RUNvY3dCcmFuN251SytURU5EMmwyZjlZcng1b1JNRU56NzB3bHlIMzZPWkJtdDBrNTk4L1doMEhEWUxaZW8wZHlTV3JOd3dlWXZTeEU4L01kbTQzWEV1U3pialR6ZnNNMHZVUndGQlNyVUxFYURPMS9JUDJVcjdCc2dId1JJL3hmb3FJbUsxS2twVXEwQWxjVEFpM3YxdTl6Qy9xTGdQd0F5UUl2dzlVQ3NpcnJQQTBZMFlPaFFJREFRQUJNQTBHQ1NxR1NJYjNEUUVCQ3dVQUE0SUJBUURjam9qZEd6L0FJQ2pqTTBaN21ZbGdQNXpic2FRNWRDMmNqZjRESnFta21zV3VmUnBDNHNic3VoODcwY0NCS2N1dmgrb0dpekJRSHJQbTRUaEl2ZklsS0w4WGpMQVhiRnVSUG9IQWcwOHNMWGR2UFRCVE52REYxTWhvcU5zMmo2ZUZxL2ROdXF2ZUJIcjVENXRLblYyWEJHRUhFOVJFOVdUa1pRT2MwaEhtQ3dNbWNZb3JYRzhCa3l1OXFwNXhyMDZMQ0htMnJLcnI2ZENRVldBV0R0MzhiS2t5STRobTVSNTVCclR5UldSdzI1RS9YaFEwVksva1FJYW9GZ0hvaWo0ekg5bmxlZnZMbmhaZDVPRzROL29OS2pBKy9LbkVqaTdPQXhKWVNaR1FmRjU0R1AwQTE4VnF1NVVGaFBKMUZFQXZ5YjR0QnZtTzM1NFFVUys5UTY2agotLS0tLUVORCBDRVJUSUZJQ0FURS0tLS0t"
}
```
