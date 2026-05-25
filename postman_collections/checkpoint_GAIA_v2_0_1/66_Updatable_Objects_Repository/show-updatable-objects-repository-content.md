# show-updatable-objects-repository-content

**Collection:** Web API (version 2.0.1) > 66 Updatable Objects Repository
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-updatable-objects-repository-content`

## Description

Show the content of the Updatable Objects Repository

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "limit": 1
}
```

## Example Responses

### Example 1: show-updatable-objects-repository-content
**Status:** `200 OK`

**Body:**
```javascript
{
  "from": 1,
  "to": 1,
  "total": 123,
  "objects": [
    {
      "name-in-updatable-objects-repository": "Amazon",
      "uid-in-updatable-objects-repository": "9f838ccf-4376-11e7-948e-005056c0000c",
      "additional-properties": {
        "description": "Amazon Web Services (abbreviated AWS) is a collection of remote computing services (also called web services) that together make up a cloud computing platform, offered over the Internet by Amazon.com.",
        "info-text": "Amazon Web Services IP address ranges info page",
        "info-url": "http://docs.aws.amazon.com/general/latest/gr/aws-ip-ranges.html",
        "uri": "/Updatable Objects/Amazon Web Services"
      }
    }
  ]
}
```
