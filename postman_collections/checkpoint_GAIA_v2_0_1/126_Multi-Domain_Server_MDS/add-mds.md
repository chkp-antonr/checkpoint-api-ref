# add-mds

**Collection:** Web API (version 2.0.1) > 126 Multi-Domain Server (MDS)
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-mds`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "mymds",
  "ip-address": "1.1.1.1",
  "server-type": "multi-domain server",
  "os": "gaia",
  "hardware": "open server",
  "ip-pool-first": "2.2.2.2",
  "ip-pool-last": "3.3.3.3"
}
```

## Example Responses

### Example 1: add-mds
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "30b2b897-9593-42ee-a443-d72bd214f9c4",
  "name": "mymds",
  "type": "mds",
  "domain": {
    "uid": "a0eebc99-afed-4ef8-bb6d-fedfedfedfed",
    "name": "System Data",
    "domain-type": "mds"
  },
  "tags": [],
  "read-only": true,
  "comments": "",
  "color": "black",
  "icon": "Objects/mds",
  "ipv4-address": "1.1.1.1",
  "ipv6-address": "",
  "os": {
    "uid": "ed01fd50-d2ba-4e0f-9001-9acf987957b0",
    "name": "Gaia",
    "type": "OS",
    "domain": {
      "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
      "name": "Check Point Data",
      "domain-type": "data domain"
    }
  },
  "version": {
    "uid": "4c48a3d2-7f38-4a72-a698-07bf5360580c",
    "name": "R81",
    "type": "CPVersion",
    "domain": {
      "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
      "name": "Check Point Data",
      "domain-type": "data domain"
    }
  },
  "hardware": {
    "uid": "c131798a-b487-4189-8f84-cc2749bc3ab1",
    "name": "Open server",
    "type": "Hardware",
    "domain": {
      "uid": "a0bbbc99-adef-4ef8-bb6d-defdefdefdef",
      "name": "Check Point Data",
      "domain-type": "data domain"
    }
  },
  "sic-name": "",
  "sic-state": "uninitialized",
  "server-type": "multi-domain server",
  "ip-pool-first": "2.2.2.2",
  "ip-pool-last": "3.3.3.3",
  "domains": [],
  "global-domains": []
}
```
