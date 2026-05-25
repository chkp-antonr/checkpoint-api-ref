# add-outbound-inspection-certificate-with-dn

**Collection:** Web API (version 2.1) > 130 Outbound Inspection Certificate
**Method:** `POST`
**URL:** `{{server}}/v2.1/add-outbound-inspection-certificate`

## Description

Add an outbound certificate object with dn.

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
  "dn": "O=Check Point, OU=R&D, C=IL",
  "base64-password": "bXlfcGFzc3dvcmQ=",
  "valid-from": "2021-04-17",
  "valid-to": "2028-04-17",
  "is-default": "false",
  "public-key-algorithm": "ecdsa-p-384"
}
```

## Example Responses

### Example 1: add-outbound-inspection-certificate-with-dn
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "f933ad42-ba13-44fa-84e5-f256e15ed7be",
  "name": "OutboundCertificate",
  "type": "outbound-inspection-certificate",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1744628987375,
      "iso-8601": "2025-04-14T14:09+0300"
    },
    "last-modifier": "aa",
    "creation-time": {
      "posix": 1744628987353,
      "iso-8601": "2025-04-14T14:09+0300"
    },
    "creator": "aa"
  },
  "available-actions": {},
  "tags": [],
  "read-only": true,
  "color": "black",
  "icon": "subject_user_certificate",
  "issued-by": "O=Check Point, OU=R&D, C=IL",
  "valid-from": "17-Apr-21",
  "valid-to": "17-Apr-28",
  "base64-certificate": "MIIEFQIBAzCCA9MGCSqGSIb3DQEHAaCCA8QEggPAMIIDvDCCAjIGCSqGSIb3DQEHAaCCAiMEggIfMIICGzCCAhcGCyqGSIb3DQEMCgEDoIIBpjCCAaIGCiqGSIb3DQEJFgGgggGSBIIBjjCCAYowggEPoAMCAQICBFSn+OEwCgYIKoZIzj0EAwIwHTEbMBkGA1UEAxMSd3d3LmNoZWNrcG9pbnQuY29tMB4XDTIxMDQxNjIxMDAwMFoXDTI4MDQxNjIxMDAwMFowHTEbMBkGA1UEAxMSd3d3LmNoZWNrcG9pbnQuY29tMHYwEAYHKoZIzj0CAQYFK4EEACIDYgAE1ZSikufAOneeYefJFLQwfgIv8REjtXMqezDwoMngVM2b0cbFJNc8EL4nCtaZlkGZ6VAT4eb4dHXVLCUG7DCgyAlAn6F08pVqdIsHhpYZY/N5jAvZt9N5FvmR7iX0XgXgoyAwHjAPBgNVHRMBAf8EBTADAQH/MAsGA1UdDwQEAwIBhjAKBggqhkjOPQQDAgNpADBmAjEAuNev0+0DmPBm0KdkFI2i2/7N87K3kKrokSaBp1SG166BjunGCI+kLbeKdSt8d5h8AjEAmzCh36+Rx6pC6bRe3V6hMtbn06FeplO/CLbxr4uMPlc+FRxq1bDrQRGs65MfWfWyMV4wOwYJKoZIhvcNAQkUMS4eLABDAE4APQB3AHcAdwAuAGMAaABlAGMAawBwAG8AaQBuAHQALgBjAG8AbQAAMB8GCSqGSIb3DQEJFTESBBBJDBTZhvKXBC8y1EVu6kyzMIIBggYJKoZIhvcNAQcBoIIBcwSCAW8wggFrMIIBZwYLKoZIhvcNAQwKAQKggfcwgfQwJwYKKoZIhvcNAQwBAzAZBBREynput+Zp+P7zZ3loj4j7eR0+wgIBAQSByDXUqJR7laIy5DSnBFDF+dvnuch+eedhrd6sxLJSpmLpXLuyTMB+MlsTlvOoKHsK1OghP719HSbq6ANj/BoGAiBWjR10reeZFxajh73XJTdbBAOYx764ck/g4H6uVlszdo54H44JxPAmtvNvdPddHXG13ZlatmJcDRPxJ4Hm2UthxezvPd6aMD2sxeRIVl1j0ZXPSMuGUg1wPcuitgSfjPXVuqqQ18/ls9fBzu3lTvzpL+VjU7IRmMsSckyd3agLKFscgaCPiCXvMV4wOwYJKoZIhvcNAQkUMS4eLABDAE4APQB3AHcAdwAuAGMAaABlAGMAawBwAG8AaQBuAHQALgBjAG8AbQAAMB8GCSqGSIb3DQEJFTESBBBJDBTZhvKXBC8y1EVu6kyzMDkwITAJBgUrDgMCGgUABBTAiIKeuHpiDoC6G/7+AvYWNs6zdwQURMp6brfmafj+82d5aI+I+3kdPsI=",
  "base64-public-certificate": "-----BEGIN CERTIFICATE-----\nMIIBijCCAQ+gAwIBAgIEVKf44TAKBggqhkjOPQQDAjAdMRswGQYDVQQDExJ3d3cu\r\nY2hlY2twb2ludC5jb20wHhcNMjEwNDE2MjEwMDAwWhcNMjgwNDE2MjEwMDAwWjAd\r\nMRswGQYDVQQDExJ3d3cuY2hlY2twb2ludC5jb20wdjAQBgcqhkjOPQIBBgUrgQQA\r\nIgNiAATVlKKS58A6d55h58kUtDB+Ai/xESO1cyp7MPCgyeBUzZvRxsUk1zwQvicK\r\n1pmWQZnpUBPh5vh0ddUsJQbsMKDICUCfoXTylWp0iweGlhlj83mMC9m303kW+ZHu\r\nJfReBeCjIDAeMA8GA1UdEwEB/wQFMAMBAf8wCwYDVR0PBAQDAgGGMAoGCCqGSM49\r\nBAMCA2kAMGYCMQC416/T7QOY8GbQp2QUjaLb/s3zsreQquiRJoGnVIbXroGO6cYI\r\nj6Qtt4p1K3x3mHwCMQCbMKHfr5HHqkLptF7dXqEy1ufToV6mU78ItvGvi4w+Vz4V\r\nHGrVsOtBEazrkx9Z9bI=\r\n-----END CERTIFICATE-----\n",
  "is-default": false,
  "public-key-algorithm": "ecdsa-p-384",
  "subject": "O=Check Point, OU=R&D, C=IL"
}
```
