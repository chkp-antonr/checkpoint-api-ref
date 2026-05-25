# set-threat-protection (remove override)

**Collection:** Web API (version 2.0.1) > 105 Threat Protection
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-threat-protection`

## Description

Remove an override from an existing profile for a specific protection. Profiles that are mentioned in the command will return to their default values.<br>In the example below, the override for "New Profile 1" is removed and returns to its default value.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "FTP Commands",
  "overrides": {
    "remove": [
      "New profile 1"
    ]
  }
}
```

## Example Responses

### Example 1: set-threat-protection (remove override)
**Status:** `200 OK`
