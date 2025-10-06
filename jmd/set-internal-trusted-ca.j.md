# set-internal-trusted-ca

```json
{
  "command": "set-internal-trusted-ca",
  "description": "Edit existing Internal CA object.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/set-internal-trusted-ca",
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
        "name": "retrieve-crl-from-http-servers",
        "description": "Whether to retrieve Certificate Revocation List from http servers.",
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
    "set internal-trusted-ca": {
      "description": "Set internal trusted ca",
      "request": "POST {{server}}/set-internal-trusted-ca\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"retrieve-crl-from-http-servers\" : \"false\",\n  \"cache-crl\" : \"false\"\n}",
      "response": "{\n  \"uid\" : \"c79b045c-6e2f-9e40-94d2-c86246db6ad4\",\n  \"name\" : \"internal_ca\",\n  \"type\" : \"internal-trusted-ca\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1703406766221,\n      \"iso-8601\" : \"2023-12-24T10:32+0200\"\n    },\n    \"last-modifier\" : \"aa\",\n    \"creation-time\" : {\n      \"posix\" : 1703079755948,\n      \"iso-8601\" : \"2023-12-20T15:42+0200\"\n    },\n    \"creator\" : \"System\"\n  },\n  \"available-actions\" : { },\n  \"tags\" : [ ],\n  \"read-only\" : true,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"Objects/account_unit\",\n  \"base64-certificate\" : \"-----BEGIN CERTIFICATE-----\\nMIIDITCCAgmgAwIBAgIBATANBgkqhkiG9w0BAQsFADBDMUEwPwYDVQQKEzhqYWd1\\nYXItdDM2My10cnVzdGVkLWNhLW1haW4tdGFrZS0yLmNoZWNrcG9pbnQuY29tLnZk\\nNWcyaDAeFw0yMzEyMTkxMzM3NDFaFw0zODAxMTkwMzE0MDdaMEMxQTA/BgNVBAoT\\nOGphZ3Vhci10MzYzLXRydXN0ZWQtY2EtbWFpbi10YWtlLTIuY2hlY2twb2ludC5j\\nb20udmQ1ZzJoMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAtXqXwyyV\\nPlFUVxQb+E9rzQi6BDbB3+TeERTnnDew00oNVMdk23gpc5AlhPVwAywmtlF+uySG\\n4poHHZ7T6uwo70CRPwxIwPLtOWp/3pfR+zhPfJ5Ngz2uiWFCDd5kYJGGRjgzjCm1\\nuTNah9MM1YoR1eQdiZwHk3o21H8gd48sDffiUPGRSTEnD4OIbMplED2MqVbLX8Pw\\nu3g9V6c4HJP+25f69oeW+In1Zznaf5xHojI2wpDY2vRTci0uXx/9aItjLFzpQmlU\\nYpBcSfFMK9x0Vp4Un4lk9e9eFGJweGxvX7WtBr0J75efwJKuTUh8XPrCw0pq6Rvc\\n0AHJTl5ChkhU0QIDAQABoyAwHjAPBgNVHRMBAf8EBTADAQH/MAsGA1UdDwQEAwIB\\nhjANBgkqhkiG9w0BAQsFAAOCAQEAtGzyJVap79j28UKFXhkJ3O5Shuj+UpwJ2vr3\\nSztqCD8OUzQi+etKd/z/vCgWa9d4ox/BNMCnPA6P35iKMXs6+BHtDb1YiaBJbTt0\\nW/W/Vfcw/cGrxDyFVb8mXLyBWJ+Z40cO2qgLmDWuJSCV+i5ja/28m81kZzMUzd1j\\n0zbv6RdQoWRpDkr2YTAhfgSjmB4CovrT+RZ0+w/jS1DcGAPevCSq8n/lIQ/yOp9S\\nu/P9EEfoj36fkeS459n/iGPb8lGa/FrzQ9B5Z6Im07RfzCgvfRfrHIu4FriWQ5VF\\neeTB23YGKhoJbFnmM6/gONuq1JUw+mSIUdJXJAnQ3CphigJJiw==\\n-----END CERTIFICATE-----\\n\",\n  \"retrieve-crl-from-http-servers\" : false,\n  \"retrieve-crl-from-ldap-servers\" : false,\n  \"cache-crl\" : false,\n  \"crl-cache-timeout\" : 1440,\n  \"allow-certificates-from-branches\" : false,\n  \"branches\" : [ ]\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:17.711738",
    "source_file": "set-internal-trusted-ca.html"
  }
}
```