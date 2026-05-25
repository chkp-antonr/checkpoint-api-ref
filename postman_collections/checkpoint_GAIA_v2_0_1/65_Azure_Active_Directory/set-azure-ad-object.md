# set-azure-ad-object

**Collection:** Web API (version 2.0.1) > 65 Azure Active Directory
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-azure-ad`

## Description

Edit Microsoft Azure Active Directory.<br>Use the show-task command to check the progress of the task. Output below is the output of the show-task command.

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
  "application-id": "a8662b33-306f-42ba-9ffb-a0ac27c7565f",
  "application-key": "EjdJ2JcNGpw3[GV8:PMN_s2KH]IyoMgh",
  "directory-id": "19c063a8-3bee-4ea5-b984-e344adsa37f7"
}
```

## Example Responses

### Example 1: set-azure-ad-object
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
