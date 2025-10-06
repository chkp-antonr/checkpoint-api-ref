# set-external-trusted-ca

```json
{
  "command": "set-external-trusted-ca",
  "description": "Edit existing object using object name or uid.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/set-external-trusted-ca",
    "headers": [
      {
        "name": "Content-Type",
        "value": "application/json",
        "description": "Send JSON object to use the API Web Services"
      },
      {
        "name": "X-chkp-sid",
        "value": "string token",
        "description": "Session unique identifier as it returned by the login request"
      }
    ],
    "body": [
      {
        "name": "uid",
        "description": "Object unique identifier.",
        "type": "string",
        "required": true
      },
      {
        "name": "base64-certificate",
        "description": "Certificate file encoded in base64.",
        "type": "string",
        "required": false
      },
      {
        "name": "retrieve-crl-from-http-servers",
        "description": "Whether to retrieve Certificate Revocation List from http servers.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "crl-cache-method",
        "description": "Weather to retrieve new Certificate Revocation List after the certificate expires or after a fixed period.",
        "type": "string",
        "required": false,
        "valid_values": [
          "timeout",
          "expiration date"
        ]
      },
      {
        "name": "crl-cache-timeout",
        "description": "When to fetch new Certificate Revocation List (in minutes).",
        "type": "integer",
        "required": false
      },
      {
        "name": "allow-certificates-from-branches",
        "description": "Allow only certificates from listed branches.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "branches",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "add",
        "description": "Adds to collection of values",
        "type": "string",
        "required": false
      },
      {
        "name": "remove",
        "description": "Removes from collection of values",
        "type": "string",
        "required": false
      }
    ]
  },
  "response": {
    "success": [
      {
        "name": "name",
        "description": "Object name. Must be unique in the domain.",
        "type": "string",
        "required": false
      },
      {
        "name": "uid",
        "description": "Object unique identifier.",
        "type": "string",
        "required": false
      },
      {
        "name": "type",
        "description": "Object type.",
        "type": "string",
        "required": false
      },
      {
        "name": "base64-certificate",
        "description": "Certificate file encoded in base64.",
        "type": "string",
        "required": false
      },
      {
        "name": "retrieve-crl-from-http-servers",
        "description": "Whether to retrieve Certificate Revocation List from http servers.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "retrieve-crl-from-ldap-servers",
        "description": "Whether to retrieve Certificate Revocation List from ldap servers.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "cache-crl",
        "description": "Cache Certificate Revocation List on the Security Gateway.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "crl-cache-method",
        "description": "Weather to retrieve new Certificate Revocation List after the certificate expires or after a fixed period.",
        "type": "string",
        "required": false,
        "valid_values": [
          "timeout",
          "expiration date"
        ]
      },
      {
        "name": "crl-cache-timeout",
        "description": "When to fetch new Certificate Revocation List (in minutes).",
        "type": "integer",
        "required": false
      },
      {
        "name": "allow-certificates-from-branches",
        "description": "Allow only certificates from listed branches.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "branches",
        "description": "Branches to allow certificates from. Required only if \"allow-certificates-from-branches\" set to \"true\".",
        "type": "array",
        "required": false
      },
      {
        "name": "tags",
        "description": "Collection of tag objects identified by the name or UID.",
        "type": "array",
        "required": false
      }
    ],
    "failure": [
      {
        "name": "message",
        "description": "Operation status.",
        "type": "string",
        "required": false
      },
      {
        "name": "warnings",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "current-session",
        "description": "Validation related to the current session.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "message",
        "description": "Validation message.",
        "type": "string",
        "required": false
      },
      {
        "name": "errors",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "current-session",
        "description": "Validation related to the current session.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "message",
        "description": "Validation message.",
        "type": "string",
        "required": false
      },
      {
        "name": "blocking-errors",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "current-session",
        "description": "Validation related to the current session.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "message",
        "description": "Validation message.",
        "type": "string",
        "required": false
      },
      {
        "name": "code",
        "description": "Error code.",
        "type": "string",
        "required": false,
        "valid_values": [
          "generic_error",
          "generic_err_invalid_syntax",
          "generic_err_invalid_parameter_name",
          "not_implemented",
          "generic_internal_error",
          "generic_server_error",
          "generic_server_initializing",
          "generic_err_command_not_found",
          "generic_err_command_version_not_found",
          "generic_err_invalid_api_type",
          "generic_err_invalid_api_object_feature",
          "generic_err_missing_required_parameters",
          "generic_err_missing_required_header",
          "generic_err_invalid_header",
          "generic_err_invalid_parameter",
          "generic_err_normalize",
          "err_bad_url",
          "err_unknown_api_version",
          "err_login_failed_wrong_username_or_password",
          "err_login_failed_more_than_one_opened_session",
          "err_login_failed",
          "err_already_connected",
          "err_normalization_failed",
          "err_validation_failed",
          "err_submit_failed",
          "err_publish_failed",
          "generic_err_missing_session_id",
          "generic_err_wrong_session_id",
          "generic_err_session_expired",
          "generic_err_session_in_use",
          "err_switch_session_failed",
          "err_connect_session_failed",
          "err_assign_session_failed",
          "err_take_over_session_failed",
          "generic_err_no_permissions",
          "err_forbidden",
          "err_not_a_system_domain_session",
          "err_inappropriate_domain_type",
          "generic_err_object_not_found",
          "generic_err_object_field_not_unique",
          "generic_err_object_type_wrong",
          "generic_err_object_locked",
          "generic_err_object_deletion",
          "err_ha_invalid_operation",
          "err_policy_installation_failed",
          "err_policy_verification_failed",
          "err_rulebase_invalid_operation",
          "err_installed_policy_mismatch",
          "err_server_certificate_operation_failed",
          "err_outbound_inspection_certificate_operation_failed",
          "err_gaia_api_login_failed",
          "err_gaia_api_send_command_failed",
          "err_cme_api_send_command_failed",
          "err_cme_api_not_running_failure",
          "err_infinity_unauthorized",
          "err_infinity_network",
          "err_too_many_requests"
        ]
      }
    ],
    "http_codes": {
      "success": [
        200
      ],
      "failure": [
        400,
        401,
        403,
        404,
        409,
        500,
        501
      ]
    }
  },
  "examples": {
    "set external-trusted-ca": {
      "description": "Set external trusted ca",
      "request": "POST {{server}}/set-external-trusted-ca\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"external_ca\",\n  \"base64-certificate\" : \"MIICujCCAaKgAwIBAgIIFbLYzT2+3TMwDQYJKoZIhvcNAQELBQAwFDESMBAGA1UEAxMJd3d3LnouY29tMB4XDTI0MDIwMTEyMzEwMFoXDTI0MTIzMTE2MDAwMFowFDESMBAGA1UEAxMJd3d3LnouY29tMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAoBreRGuq8u43GBog+ZaAnaR8ZF8cT2ppvtd3JoFmzTOQivLIt9sNtFYqEgHCtnNkKn9TRrxN14YscHgKIxfDSVlC9Rh0rrBvWgFqcm715Whr99Ogx6JbYFkusFWJarSejIFx4n6MM48MJxLdtCP6Hy1G2cj1BCiCHj4i3VIVaDE/aMkSqJbYEvf+vFqUWxY8/uEuKI/HGhI7mhUPW4NSGL0Oafz5eEFVsxqV5NA19/JJZ9NajSkyANnaNL5raxGV0oeqaE3JB3lSEZfWbH6mQsToUxxwIQfsZiIBozajDdTgP3Kn4SMY0b+I/WAWgfigMSDTAIR8J1sdzGXy2w2kqQIDAQABoxAwDjAMBgNVHRMEBTADAQH/MA0GCSqGSIb3DQEBCwUAA4IBAQBxaE9O/LCjKfWeugPeDPvr3Ld0i1mYsgNIyN+ES1iDoJHXrBQpVzZelJRr8leFgbghGUX7Fwdh1qZ2Jw6nmD1oe/Q7jkPzTngb6dIMI/kFK4eXcS4GJ3S7yGobLB7QUKK1vrYWZdNuAzR6jMRmFECS+lPF7zlTexnwwOkATMp6lzS7xEpEhk/8eLpSQnYzvsM+rL9voU5q9MrdAJ2XaCZe4Crv75NdYU6ljD2eSYDrO148Tg480TlvT5wzBuyanKhI/Po2oLEVWU7h5tkensHKB5zvxigIr9ZkczdzVbbrRFi2jSQy+VxYWc0zCo/uO+yaKmmLfGDQEb8wZYY1Ml27\",\n  \"retrieve-crl-from-http-servers\" : \"false\",\n  \"crl-cache-method\" : \"expiration date\"\n}",
      "response": "{\n  \"uid\" : \"bae2e0c7-4667-49a8-95c7-1ce9d7cd6584\",\n  \"name\" : \"external_ca\",\n  \"type\" : \"external-trusted-ca\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1703162491765,\n      \"iso-8601\" : \"2023-12-21T14:41+0200\"\n    },\n    \"last-modifier\" : \"aa\",\n    \"creation-time\" : {\n      \"posix\" : 1703162491765,\n      \"iso-8601\" : \"2023-12-21T14:41+0200\"\n    },\n    \"creator\" : \"aa\"\n  },\n  \"available-actions\" : {\n    \"edit\" : \"true\",\n    \"delete\" : \"true\",\n    \"clone\" : \"true\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : false,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"Objects/account_unit\",\n  \"base64-certificate\" : \"-----BEGIN CERTIFICATE-----\\nMIICujCCAaKgAwIBAgIIFbLYzT2+3TMwDQYJKoZIhvcNAQELBQAwFDESMBAGA1UE\\nAxMJd3d3LnouY29tMB4XDTI0MDIwMTEyMzEwMFoXDTI0MTIzMTE2MDAwMFowFDES\\nMBAGA1UEAxMJd3d3LnouY29tMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKC\\nAQEAoBreRGuq8u43GBog+ZaAnaR8ZF8cT2ppvtd3JoFmzTOQivLIt9sNtFYqEgHC\\ntnNkKn9TRrxN14YscHgKIxfDSVlC9Rh0rrBvWgFqcm715Whr99Ogx6JbYFkusFWJ\\narSejIFx4n6MM48MJxLdtCP6Hy1G2cj1BCiCHj4i3VIVaDE/aMkSqJbYEvf+vFqU\\nWxY8/uEuKI/HGhI7mhUPW4NSGL0Oafz5eEFVsxqV5NA19/JJZ9NajSkyANnaNL5r\\naxGV0oeqaE3JB3lSEZfWbH6mQsToUxxwIQfsZiIBozajDdTgP3Kn4SMY0b+I/WAW\\ngfigMSDTAIR8J1sdzGXy2w2kqQIDAQABoxAwDjAMBgNVHRMEBTADAQH/MA0GCSqG\\nSIb3DQEBCwUAA4IBAQBxaE9O/LCjKfWeugPeDPvr3Ld0i1mYsgNIyN+ES1iDoJHX\\nrBQpVzZelJRr8leFgbghGUX7Fwdh1qZ2Jw6nmD1oe/Q7jkPzTngb6dIMI/kFK4eX\\ncS4GJ3S7yGobLB7QUKK1vrYWZdNuAzR6jMRmFECS+lPF7zlTexnwwOkATMp6lzS7\\nxEpEhk/8eLpSQnYzvsM+rL9voU5q9MrdAJ2XaCZe4Crv75NdYU6ljD2eSYDrO148\\nTg480TlvT5wzBuyanKhI/Po2oLEVWU7h5tkensHKB5zvxigIr9ZkczdzVbbrRFi2\\njSQy+VxYWc0zCo/uO+yaKmmLfGDQEb8wZYY1Ml27\\n-----END CERTIFICATE-----\\n\",\n  \"retrieve-crl-from-http-servers\" : false,\n  \"retrieve-crl-from-ldap-servers\" : false,\n  \"cache-crl\" : true,\n  \"crl-cache-method\" : \"expiration date\",\n  \"crl-cache-timeout\" : 1440,\n  \"allow-certificates-from-branches\" : false,\n  \"branches\" : [ ]\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:16.737442",
    "source_file": "set-external-trusted-ca.html"
  }
}
```