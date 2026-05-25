# add data-center-server type VMware NSX-T

**Collection:** Web API (version 2.1) > 73 Data Center Server
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-data-center-server`

## Description

Add data center server of type VMware NSX-T,<br>Use the show-task command to check the progress of the task. Output below is the output of the show-task command.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "my_nsxt",
  "type": "nsxt",
  "username": "admin",
  "password-base64": "YWRtaW4=",
  "hostname": "127.0.0.1",
  "certificate-fingerprint": "4f4f4676712a43460a7dbc2d343176dc1135a4d2"
}
```

## Example Responses

### Example 1: add data-center-server type VMware NSX-T
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
