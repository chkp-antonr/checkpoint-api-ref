# add-azure-ad-object

**Collection:** Web API (version 2.1) > 76 Azure Active Directory
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-azure-ad`

## Description

Add Microsoft Azure Active Directory.<br>Use the show-task command to check the progress of the task. Output below is the output of the show-task command.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "my_azureAD",
  "authentication-method": "service-principal-authentication",
  "application-id": "a8662b33-306f-42ba-9ffb-a0ac27c8903f",
  "application-key": "EjdJ2JcNGpw3[GV8:PMN_s2KH]JhtlpO",
  "directory-id": "19c063a8-3bee-4ea5-b984-e344asds37f7"
}
```

## Example Responses

### Example 1: add-azure-ad-object
**Status:** `200 OK`

**Body:**
```javascript
{
  "tasks": [
    {
      "task-name": "Data Center Operation",
      "task-id": "01234567-89ab-cdef-b4ab-a5aefde29b2e",
      "status": "succeeded",
      "progress-percentage": 100,
      "suppressed": false,
      "task-details": []
    }
  ]
}
```
