# get attachment by attachment-id

**Collection:** Web API (version 2.0.1) > 156 Logs
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/get-attachment`

## Description

Request for packet capture or blob data from Log server or Gateway by attacgmnet id.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "attachment-id": "MjY5HlNtYXJ0RGVmZW5zZR5jbj1jcF9tZ210LG89aHVnbzEtYmxvYkFwaS1uZXctdGFrZS0yLmNoZWNrcG9pbnQuY29tLnM2MjdvMx57MHg1OTg4"
}
```

## Example Responses

### Example 1: get attachment by attachment-id
**Status:** `200 OK`
