# set-threat-profile (set malicious mail policy settings)

**Collection:** Web API (version 2.1) > 117 Threat Profile
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-threat-profile`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "New Profile 1",
  "malicious-mail-policy-settings": {
    "email-action": "allow",
    "remove-attachments-and-links": "true",
    "malicious-attachments-text": "Original attachment $filename$ found malicious and removed by Check Point.",
    "add-x-header-to-email": "true",
    "add-email-subject-prefix": "true",
    "email-subject-prefix-text": "malicious email - ",
    "add-customized-text-to-email-body": "true",
    "send-copy": "true",
    "send-copy-list": {
      "add": "test@checkpoint.com"
    }
  }
}
```

## Example Responses

### Example 1: set-threat-profile (set malicious mail policy settings)
**Status:** `200 OK`
