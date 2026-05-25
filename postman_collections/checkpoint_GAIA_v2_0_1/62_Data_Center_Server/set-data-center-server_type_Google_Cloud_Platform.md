# set-data-center-server type Google Cloud Platform

**Collection:** Web API (version 2.0.1) > 62 Data Center Server
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/set-data-center-server`

## Description

Set the authentication method of a data center server of type Google Cloud Platform.<br>Make sure to provide all the required arguments for the new authentication method,<br>Use the show-task command to check the progress of the task. Output below is the output of the show-task command.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "my_gcp",
  "authentication-method": "key-authentication",
  "private-key": "wzVi9CcnFIT09JOFV1c0ZQRW9OQmtKU1k4UGxjeWlOXG5TZ1loV3FhZ2tITkl1RmE5MnhkMXJQMy9ZajFKWjVYeUdmM0FYZ3ZndFFLQmdRQyszNkVPQVdua01YZlByR0pQXG5rcmtEelJHNERnVTNNTDcwRkpCZldYbXBNaVAzQm53ZHljTkU0L0E4Zjh1RWpVOE0zU3FZWEtGbURIUDFwR1RxXG5yTzFFNnQzaVVTR2IrQkpMZjV6MGMweEM1SjVWM0VUYlNVT25sNXVOZXNhZUFWd0hDZncvY2Y1WDRjUlZQU1V0XG50S1Q3Q2Q1MXRBUUxFdm5TUC9FVXhZL0Qyd0tCZ1FDMWlSa1FqcndwUmVLUFlwRkJWSnAQ09nckhBbXdRa2hFa096clVtS3BOZURrRFlEMVV6cjY3Nk9ZXG5DdmR2YWRhdGEveDUwOS9ndXloaWwlNDBjaGtwLWRldi5pYW0uZ3NlcnZpY2VhY2NvdW50LmNvbSIKfQo="
}
```

## Example Responses

### Example 1: set-data-center-server type Google Cloud Platform
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
