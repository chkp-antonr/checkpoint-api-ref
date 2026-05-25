# renew-scaled-sharing-server-certificate

**Collection:** Web API (version 2.1) > 61 Gateways & Clusters
**Method:** `POST`
**URL:** `{{server}}/v2.1/renew-scaled-sharing-server-certificate`

## Description

Renews the server certificate for the scaled sharing on the specified PDP Security Gateway or Cluster.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "gw1"
}
```

## Example Responses

### Example 1: renew-scaled-sharing-server-certificate
**Status:** `200 OK`

**Body:**
```javascript
{
  "message": "OK"
}
```
