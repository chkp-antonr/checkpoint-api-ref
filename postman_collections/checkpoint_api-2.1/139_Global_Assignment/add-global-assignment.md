# add-global-assignment

**Collection:** Web API (version 2.1) > 139 Global Assignment
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-global-assignment`

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
