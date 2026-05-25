# add-data-center-server type Oracle Cloud

**Collection:** Web API (version 2.0.1) > 62 Data Center Server
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-data-center-server`

## Description

Add data center server of type Oracle Cloud,<br>Use the show-task command to check the progress of the task. Output below is the output of the show-task command.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "my_oci",
  "type": "oci",
  "authentication-method": "key-authentication",
  "key-user": "OCI_KEY",
  "key-tenant": "OCI_TENANT",
  "key-region": "eu-frankfurt-1",
  "private-key": "OCI_PRIVATE_KEY"
}
```

## Example Responses

### Example 1: add-data-center-server type Oracle Cloud
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
