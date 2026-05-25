# add-data-center-server type Cisco ACI

**Collection:** Web API (version 2.0.1) > 62 Data Center Server
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-data-center-server`

## Description

Add data center server of type Cisco ACI,<br>Acceptable format(s) for the URLs argument: http(s)://&lt;host&gt;:&lt;port&gt;/&lt;url&gt;.<br>Use the show-task command to check the progress of the task. Output below is the output of the show-task command.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "my_aci",
  "type": "aci",
  "urls": [
    "https://1.1.1.1"
  ],
  "username": "admin",
  "password-base64": "YWRtaW4=",
  "certificate-fingerprint": "4f4f4676712a43460a7dbc2d343176dc1135a4d2"
}
```

## Example Responses

### Example 1: add-data-center-server type Cisco ACI
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
