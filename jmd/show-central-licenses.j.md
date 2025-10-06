# show-central-licenses

```json
{
  "command": "show-central-licenses",
  "description": "Show attached licenses.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/show-central-licenses",
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
    ]
  },
  "response": {
    "success": [
      {
        "name": "licenses",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "central",
        "description": "Indicates whether the license is central or local.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "ck",
        "description": "A unique identifier which represent a specific license.",
        "type": "string",
        "required": false
      },
      {
        "name": "expiration",
        "description": "The license expiration date.",
        "type": "string",
        "required": false
      },
      {
        "name": "ip-address",
        "description": "The license IP address.",
        "type": "string",
        "required": false
      },
      {
        "name": "signature",
        "description": "The license signature.",
        "type": "string",
        "required": false
      },
      {
        "name": "sku",
        "description": "An several alpha-numeric strings separated by a dash used to define the functionality of a specific license.",
        "type": "string",
        "required": false
      },
      {
        "name": "additional-info",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "pool",
        "description": "The pool type is defined by the blades contained in the licenses of this pool.",
        "type": "string",
        "required": false
      },
      {
        "name": "quota-unit",
        "description": "The unit of the quota.",
        "type": "string",
        "required": false
      },
      {
        "name": "quota-value",
        "description": "The number of virtual cores the license covers, as specified when purchased.",
        "type": "string",
        "required": false
      },
      {
        "name": "type",
        "description": "The typ of the license.",
        "type": "string",
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
    "Show the current attached licenses": {
      "description": "",
      "request": "POST {{server}}/show-central-licenses\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{ }",
      "response": "{\n  \"licenses\" : [ {\n    \"ck\" : \"CK-777773333\",\n    \"sku\" : \"CPSG-VE+3 CPBS-BECE CPSB-DFW CPSM-C-2 CPSB-VPN CPSB-NPM CPSB-LOGS CPSB-IA CPSB-ADNC CPSB-SSLVWPN-5\",\n    \"central\" : \"true\",\n    \"expiration\" : \"never\",\n    \"ip-address\" : \"192.168.1.1\",\n    \"signature\" : \"dLLLLL-WWWWWW-ZZZZZZ-QQQQQQ\",\n    \"additional-info\" : {\n      \"type\" : \"cloud\",\n      \"pool\" : \"FIREWALL\",\n      \"quota-value\" : \"3\",\n      \"quota-unit\" : \"cores\"\n    }\n  }, {\n    \"CK\" : \"CHECK-POINT-INTERNAL-USE-ONLY\",\n    \"SKU\" : \"CPSB-BASE CPSB-FW CPSM-C-2 CPSB-VPN\",\n    \"central\" : \"true\",\n    \"expiration\" : \"2023-04-25\",\n    \"ip-address\" : \"192.168.1.1\",\n    \"signature\" : \"dTIIIIII-RRRRRR-SSSSSSS-PPPPPP\"\n  } ]\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:23.178993",
    "source_file": "show-central-licenses.html"
  }
}
```