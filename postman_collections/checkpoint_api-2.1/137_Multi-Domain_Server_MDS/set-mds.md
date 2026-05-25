# set-mds

**Collection:** Web API (version 2.1) > 137 Multi-Domain Server (MDS)
**Method:** `POST`
**URL:** `{{server}}/v2.1/set-mds`

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
  "ip-address": "1.2.3.4",
  "os": "linux",
  "hardware": "Smart-1"
}
```

## Example Responses

### Example 1: set-mds
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
  "ipv4-address": "1.2.3.4",
  "ipv6-address": "",
  "os": {
    "uid": "d4ab612d-9fdc-4f5e-afe6-9a72d1d85e24",
    "name": "Linux",
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
    "uid": "018e1a9f-7597-46d3-88b1-7b7611cc343e",
    "name": "Smart-1",
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
