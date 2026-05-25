# show-azure-ad-object

**Collection:** Web API (version 2.0.1) > 65 Azure Active Directory
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-azure-ad`

## Description

Show Microsoft Azure Active Directory.<br>Use the show-task command to check the progress of the task. Output below is the output of the show-task command.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "my_azureAD"
}
```

## Example Responses

### Example 1: show-azure-ad-object
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "f3047481-b752-46ac-b54b-753cd32720eb",
  "name": "my_azureAD",
  "type": "Azure AD",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "locked by current session",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1581346950230,
      "iso-8601": "2020-02-10T17:02+0200"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1581346950230,
      "iso-8601": "2020-02-10T17:02+0200"
    },
    "creator": "aa"
  },
  "tags": [],
  "read-only": false,
  "comments": "",
  "color": "black",
  "icon": "NetworkObjects/ExternalDataSource",
  "properties": [
    {
      "name": "Azure_User_Name",
      "value": ""
    },
    {
      "name": "Azure_Tenant_Id",
      "value": "19c063a8-3bee-4ea5-b984-e344adaa37f7"
    },
    {
      "name": "Azure_Client_Id",
      "value": "a8662b33-306f-42ba-9ffb-a0ac27c7563f"
    }
  ]
}
```
