# delete external-trusted-ca

**Collection:** Web API (version 2.0.1) > 34 External Trusted CA
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/delete-external-trusted-ca`

## Description

Delete external trusted ca

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "external_ca"
}
```

## Example Responses

### Example 1: delete external-trusted-ca
**Status:** `200 OK`
