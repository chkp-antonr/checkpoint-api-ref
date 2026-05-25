# Clone a Domain on the Multi-Domain Security Management Server

**Collection:** Web API (version 2.1) > 135 Domain
**Method:** `POST`
**URL:** `{{server}}/v2.1/clone-domain`

## Description

Clone the Domain "domain1" to the new Domain "domain2". The name of the new Domain Server is "domain2_Server". The IPv4 address of the new Domain Server is "192.0.2.1".

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "domain1",
  "new-domain-name": "domain2",
  "new-domain-server-name": "domain2_Server",
  "new-domain-server-ip": "192.0.2.1"
}
```

## Example Responses

### Example 1: Clone a Domain on the Multi-Domain Security Management Server
**Status:** `200 OK`
