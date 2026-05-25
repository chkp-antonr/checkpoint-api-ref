# add-outbound-inspection-certificate

**Collection:** Web API (version 2.0.1) > 119 Outbound Inspection Certificate
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/add-outbound-inspection-certificate`

## Description

Add an outbound certificate object.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "name": "OutboundCertificate",
  "issued-by": "www.checkpoint.com",
  "base64-password": "bXlfcGFzc3dvcmQ=",
  "valid-from": "2021-04-17",
  "valid-to": "2028-04-17",
  "is-default": "false"
}
```

## Example Responses

### Example 1: add-outbound-inspection-certificate
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "d14a2df3-467f-44b8-b1ed-59d8e1af6d91",
  "name": "OutboundCertificate",
  "type": "outbound-inspection-certificate",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "icon": "subject_user_certificate",
  "issued-by": "CN=www.checkpoint.com",
  "valid-from": "17-Apr-21",
  "valid-to": "17-Apr-28",
  "base64-certificate": "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",
  "public-certificate": "-----BEGIN CERTIFICATE-----\nMIIC2DCCAcCgAwIBAgIEWxZcFjANBgkqhkiG9w0BAQsFADAdMRswGQYDVQQDExJ3\r\nd3cuY2hlY2twb2ludC5jb20wHhcNMjEwNDE2MjEwMDAwWhcNMjgwNDE2MjEwMDAw\r\nWjAdMRswGQYDVQQDExJ3d3cuY2hlY2twb2ludC5jb20wggEiMA0GCSqGSIb3DQEB\r\nAQUAA4IBDwAwggEKAoIBAQDUXtFLKbsE4Km8Ddf9ZJ9igNdZRX/t+bUQMeJv4yCB\r\nYx7zGkP8Jq7O0Z9lp2G/x9BFKRkqyONKsNZMeQ8nVK8ZyhxqbYq1cacbTgInv/5U\r\nuNT1J+S9oktEPrAdlWHdNmclecCGBPDUvSv45CiP7ntJ60pKagWZbn1YHzl9QfYT\r\n41UODfBxSipYu/ijT9o6BDpaZHozr7InSG9k4Upgu7RfIaONHqhET02hmijWsZc8\r\nAdIKbcZixo9qfeW/lz8mM2e1VetVSwAngpqk/jHCugZyiaMQcnq23GsUqJGYcdDs\r\nmHfuXsWtBjhbzc0X4nqZGvws96YsjMZkocFKXd/NTkh5AgMBAAGjIDAeMA8GA1Ud\r\nEwEB/wQFMAMBAf8wCwYDVR0PBAQDAgGGMA0GCSqGSIb3DQEBCwUAA4IBAQCuDQnj\r\nDBmYZF84bcF2OeoCIRURLOpZPev6J1jLdklbIbco+yZHZ741hMiHj2CRgBP+m8ZM\r\nyYT+dC6pPTJ2HhhgMkO3E31Av814aryoJD/rc9PybcB99ykjfbj7gDXwB5rajwLO\r\nD0raXogErCMP2lyYLpmzsDrY7GsQEjm+4RlYL0smQX0DVgp4+7ScHPXx6JmtpW7R\r\n7w3EEf0sZvEvcXgwlLS9OwshvUVeG5TtomFiT2K2X8KdZrJboJybpAFA6nNRS91m\r\n6KOteJUZdkyyvqYCG9WJH020CwJmEcjUaw0zBbYtoUYsCllfnEBrF10MgLQdPG9U\r\n4ldtw4SrpaJBwpGk\r\n-----END CERTIFICATE-----\n",
  "is-default": false
}
```
