# get attachment by attachment-id

**Collection:** Web API (version 2.1) > 173 Logs
**Method:** `POST`
**URL:** `{{server}}/v2.1/get-attachment`

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
