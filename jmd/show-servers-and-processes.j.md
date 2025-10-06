# show-servers-and-processes

```json
{
  "command": "show-servers-and-processes",
  "description": "Shows the status of all processes in the current machine (Multi-Domain Server and all Domain Management / Log Servers). This command is available only on Multi-Domain Server.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/show-servers-and-processes",
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
        "name": "servers",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "mds",
          "data domain",
          "domain",
          "global domain"
        ]
      },
      {
        "name": "name",
        "description": "Object name. Must be unique in the domain.",
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
        "name": "ip-address",
        "description": "IPv4 or IPv6 address.",
        "type": "string",
        "required": false
      },
      {
        "name": "server-status",
        "description": "Server status.",
        "type": "string",
        "required": false
      },
      {
        "name": "processes",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "name",
        "description": "Process name.",
        "type": "string",
        "required": false
      },
      {
        "name": "pid",
        "description": "Process id.",
        "type": "string",
        "required": false
      },
      {
        "name": "status",
        "description": "Process status.",
        "type": "string",
        "required": false
      },
      {
        "name": "domain",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "mds",
          "data domain",
          "domain",
          "global domain"
        ]
      },
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
        "name": "domain-type",
        "description": "Domain type.",
        "type": "string",
        "required": false,
        "valid_values": [
          "mds",
          "data domain",
          "domain",
          "global domain"
        ]
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
    "show-servers-and-processes": {
      "description": "",
      "request": "POST {{server}}/show-servers-and-processes\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{ }\n\n \u2022 This command is available only after logging in to the System Data domain.",
      "response": "{\n  \"servers\" : [ {\n    \"name\" : \"MyMDS\",\n    \"type\" : \"mds\",\n    \"domain\" : {\n      \"uid\" : \"a0eebc99-afed-4ef8-bb6d-fedfedfedfed\",\n      \"name\" : \"System Data\",\n      \"domain-type\" : \"mds\"\n    },\n    \"ip-address\" : \"1.2.3.4\",\n    \"server-status\" : \"up\",\n    \"processes\" : [ {\n      \"name\" : \"FWM\",\n      \"status\" : \"up\",\n      \"pid\" : \"19242\"\n    }, {\n      \"name\" : \"FWMHA\",\n      \"status\" : \"up\",\n      \"pid\" : \"19247\"\n    }, {\n      \"name\" : \"FWD\",\n      \"status\" : \"up\",\n      \"pid\" : \"19236\"\n    }, {\n      \"name\" : \"CPD\",\n      \"status\" : \"up\",\n      \"pid\" : \"9233\"\n    }, {\n      \"name\" : \"CPCA\",\n      \"status\" : \"up\",\n      \"pid\" : \"19643\"\n    } ]\n  }, {\n    \"name\" : \"cma1\",\n    \"type\" : \"domain-server\",\n    \"domain\" : {\n      \"uid\" : \"de7830c8-9c44-4c6d-b6dd-1e3d115d5893\",\n      \"name\" : \"domain1\",\n      \"domain-type\" : \"domain\"\n    },\n    \"ip-address\" : \"1.1.1.1\",\n    \"server-status\" : \"up\",\n    \"processes\" : [ {\n      \"name\" : \"FWM\",\n      \"status\" : \"up\",\n      \"pid\" : \"17470\"\n    }, {\n      \"name\" : \"FWMHA\",\n      \"status\" : \"up\",\n      \"pid\" : \"17387\"\n    }, {\n      \"name\" : \"FWD\",\n      \"status\" : \"up\",\n      \"pid\" : \"17796\"\n    }, {\n      \"name\" : \"CPD\",\n      \"status\" : \"up\",\n      \"pid\" : \"17181\"\n    }, {\n      \"name\" : \"CPCA\",\n      \"status\" : \"up\",\n      \"pid\" : \"19576\"\n    } ]\n  }, {\n    \"name\" : \"cma2\",\n    \"type\" : \"domain-server\",\n    \"domain\" : {\n      \"uid\" : \"0b60613e-0c62-441f-9b2d-1b2a850b7fa4\",\n      \"name\" : \"domain2\",\n      \"domain-type\" : \"domain\"\n    },\n    \"ip-address\" : \"2.2.2.2\",\n    \"server-status\" : \"up\",\n    \"processes\" : [ {\n      \"name\" : \"FWM\",\n      \"status\" : \"up\",\n      \"pid\" : \"17162\"\n    }, {\n      \"name\" : \"FWMHA\",\n      \"status\" : \"up\",\n      \"pid\" : \"17858\"\n    }, {\n      \"name\" : \"FWD\",\n      \"status\" : \"up\",\n      \"pid\" : \"17389\"\n    }, {\n      \"name\" : \"CPD\",\n      \"status\" : \"up\",\n      \"pid\" : \"17111\"\n    }, {\n      \"name\" : \"CPCA\",\n      \"status\" : \"up\",\n      \"pid\" : \"19569\"\n    } ]\n  } ]\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:27.355327",
    "source_file": "show-servers-and-processes.html"
  }
}
```