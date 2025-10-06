# show-opsec-trusted-ca

```json
{
  "command": "show-opsec-trusted-ca",
  "description": "Retrieve existing object using object name or uid.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/show-opsec-trusted-ca",
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
        "name": "automatic-enrollment",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "scep",
          "cmpv2",
          "cmpv1"
        ]
      },
      {
        "name": "automatically-enroll-certificate",
        "description": "Whether to automatically enroll certificate.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "protocol",
        "description": "Protocol that communicates with the certificate authority. Available only if \"automatically-enroll-certificate\" parameter is set to true.",
        "type": "string",
        "required": false,
        "valid_values": [
          "scep",
          "cmpv2",
          "cmpv1"
        ]
      },
      {
        "name": "scep-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "ca-identifier",
        "description": "Certificate authority identifier.",
        "type": "string",
        "required": false
      },
      {
        "name": "url",
        "description": "Certificate authority URL.",
        "type": "string",
        "required": false
      },
      {
        "name": "cmpv1-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "direct-tcp-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "ip-address",
        "description": "Certificate authority IP address.",
        "type": "string",
        "required": false
      },
      {
        "name": "port",
        "description": "Port number.",
        "type": "integer",
        "required": false
      },
      {
        "name": "cmpv2-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "http",
          "direct-tcp"
        ]
      },
      {
        "name": "transport-layer",
        "description": "Transport layer.",
        "type": "string",
        "required": false,
        "valid_values": [
          "http",
          "direct-tcp"
        ]
      },
      {
        "name": "direct-tcp-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "ip-address",
        "description": "Certificate authority IP address.",
        "type": "string",
        "required": false
      },
      {
        "name": "port",
        "description": "Port number.",
        "type": "integer",
        "required": false
      },
      {
        "name": "http-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "url",
        "description": "Certificate authority URL.",
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
    "show opsec-trusted-ca": {
      "description": "Show opsec trusted ca",
      "request": "POST {{server}}/show-opsec-trusted-ca\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"opsec_ca\"\n}",
      "response": "{\n  \"uid\" : \"24dfc6a6-a0a3-4d12-90e5-295d9790f3b9\",\n  \"name\" : \"opsec_ca\",\n  \"type\" : \"opsec-trusted-ca\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"locked by current session\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1703170011352,\n      \"iso-8601\" : \"2023-12-21T16:46+0200\"\n    },\n    \"last-modifier\" : \"aa\",\n    \"creation-time\" : {\n      \"posix\" : 1703170011352,\n      \"iso-8601\" : \"2023-12-21T16:46+0200\"\n    },\n    \"creator\" : \"aa\"\n  },\n  \"available-actions\" : {\n    \"edit\" : \"true\",\n    \"delete\" : \"true\",\n    \"clone\" : \"false\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : false,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"Objects/account_unit\",\n  \"base64-certificate\" : \"-----BEGIN CERTIFICATE-----\\nMIICwjCCAaqgAwIBAgIILdexblpVEMIwDQYJKoZIhvcNAQELBQAwGDEWMBQGA1UE\\nAxMNd3d3Lm9wc2VjLmNvbTAeFw0yMzA2MjUwOTE3MDBaFw0yNTAzMzExNjAwMDBa\\nMBgxFjAUBgNVBAMTDXd3dy5vcHNlYy5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IB\\nDwAwggEKAoIBAQCjpqCxDaVg+I1b+wqnmjjYtL3v7Tlu/YpMbsKnv+M1gRz6QFUO\\noSVnxKLo0A7Y4kCqa1OPcHO/LtXuok43F1YZPVKm3xWpY8FmqGqf5ZuGmSwm1HPO\\nbcMjwGOyFgwpwEDF5e0UMZ7xtJF8BZ5KKBh3ZfQ1FbmbVqSUPcmOi+NE4JspPlHx\\nX+m6es/yeSGR1A2ezKY7KePTlwVtDe8hiLrYyKG92nka5rkD1QyEIVJ0W5wrnU4n\\nGEDIHeOfT09zroQxaNLkb51sl4Tog/qw+EraVGIBe/iFnSJoDF37i2mLJqI/t8be\\nl+aGDAxgMx1pO85OClgjPSWL0UIXGI2xrR+JAgMBAAGjEDAOMAwGA1UdEwQFMAMB\\nAf8wDQYJKoZIhvcNAQELBQADggEBAHTs1AutAmSLHF2KRLJtrRNkso0lMyA7XI7k\\n1TNpTk7TCZLNY0VbUliGbcl+POH4EG8ARUrftnwRDCTBd2BdJTqG2CyNADi+bw8a\\nLvbxok7KH0GlQvGjyfq+sHK12wTl4ULNyYoAPZ01GhXOvkobROdSyjxvBVhxdVo9\\n0kj7mHFv3N83huNhfstDFUBcQCmMkbLuzDUZrl2a1OtqlOdNC6mNvb7Jq9W9vRxG\\nA514e7jqyoM+PwHu5fILx/jmGT8suOUnvbtcDdFhjqixAPer6uSPR0CSbiJvuDy7\\n2DPH5mjZK5dQKewNYOZ/BQEsRIBe+Q6eGAoJqi+cD63cwlw0DCc=\\n-----END CERTIFICATE-----\\n\",\n  \"retrieve-crl-from-http-servers\" : true,\n  \"retrieve-crl-from-ldap-servers\" : false,\n  \"cache-crl\" : true,\n  \"crl-cache-method\" : \"timeout\",\n  \"crl-cache-timeout\" : 1440,\n  \"allow-certificates-from-branches\" : false,\n  \"branches\" : [ ],\n  \"automatic-enrollment\" : {\n    \"automatically-enroll-certificate\" : false\n  }\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:26.601922",
    "source_file": "show-opsec-trusted-ca.html"
  }
}
```