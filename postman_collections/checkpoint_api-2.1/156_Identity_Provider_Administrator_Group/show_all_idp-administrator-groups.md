# show all idp-administrator-groups

**Collection:** Web API (version 2.1) > 156 Identity Provider Administrator Group
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-idp-administrator-groups`

## Description

show all groups

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

### Example 1: show all idp-administrator-groups
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 2,
  "total": 2,
  "objects": [
    {
      "uid": "055b2f2f-06a2-48df-922b-47ddfd46f0f8",
      "name": "my global group",
      "type": "idp-administrator-group",
      "domain": {
        "uid": "a0eebc99-afed-4ef8-bb6d-fedfedfedfed",
        "name": "System Data",
        "domain-type": "mds"
      },
      "icon": "General/AdministratorGroup",
      "color": "black"
    },
    {
      "uid": "799fba94-d915-46d0-82a6-6e6bf369e87c",
      "name": "my super group",
      "type": "idp-administrators-group",
      "domain": {
        "uid": "a0eebc99-afed-4ef8-bb6d-fedfedfedfed",
        "name": "System Data",
        "domain-type": "mds"
      },
      "icon": "General/AdministratorGroup",
      "color": "black"
    }
  ]
}
```
