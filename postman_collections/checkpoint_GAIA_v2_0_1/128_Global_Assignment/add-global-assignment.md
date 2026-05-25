# add-global-assignment

**Collection:** Web API (version 2.0.1) > 128 Global Assignment
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-global-assignment`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "global-domain": "Global",
  "dependent-domain": "domain2",
  "global-access-policy": "standard",
  "global-threat-prevention-policy": "standard",
  "manage-protection-actions": true
}
```

## Example Responses

### Example 1: add-global-assignment
**Status:** `200 OK`
