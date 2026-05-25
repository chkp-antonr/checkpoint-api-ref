# show-threat-ioc-feeds

**Collection:** Web API (version 2.0.1) > 108 Threat IOC feed
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-threat-ioc-feeds`

## Description

Showing a list of threat IOC feeds

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{}
```

## Example Responses

### Example 1: show-threat-ioc-feeds
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 11,
  "total": 11,
  "objects": [
    {
      "uid": "04bec96b-0e24-48af-81f8-a9f0ed1142ca",
      "name": "Cheese6",
      "type": "threat-ioc-feed",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    },
    {
      "uid": "a78db3b2-0030-4152-9fbe-fffb117b616c",
      "name": "Cheese6",
      "type": "threat-ioc-feed",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    },
    {
      "uid": "b4386e63-78f1-412a-9cad-4ee6f7b2445a",
      "name": "Cheese7",
      "type": "threat-ioc-feed",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    },
    {
      "uid": "8dc499b0-a939-4800-93f5-fcfbba1d69d6",
      "name": "Cheese8",
      "type": "threat-ioc-feed",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    },
    {
      "uid": "b55cd1d4-98a6-45b3-8b09-00d803f2ceef",
      "name": "Cheese8",
      "type": "threat-ioc-feed",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    },
    {
      "uid": "cf9ce11d-ee79-4020-8c02-ecada00f908c",
      "name": "flaf2",
      "type": "threat-ioc-feed",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    },
    {
      "uid": "5a916ffc-0c2e-4011-9e8d-de827c830cac",
      "name": "flaf2",
      "type": "threat-ioc-feed",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    },
    {
      "uid": "398986f2-ee71-4c35-b7dd-b8dd5f720451",
      "name": "ioc_feed",
      "type": "threat-ioc-feed",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    },
    {
      "uid": "0d8b0e0e-bdfc-4512-a161-131a21260ea5",
      "name": "ioc_feed3",
      "type": "threat-ioc-feed",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    },
    {
      "uid": "7fb9b4a3-7384-4063-9b63-d2ff2f1831d0",
      "name": "ioc_feed4",
      "type": "threat-ioc-feed",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    },
    {
      "uid": "6dc0bfc0-1e12-4400-a093-84511bc2a702",
      "name": "ioc_feed5",
      "type": "threat-ioc-feed",
      "domain": {
        "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
        "name": "SMC User",
        "domain-type": "domain"
      }
    }
  ]
}
```
