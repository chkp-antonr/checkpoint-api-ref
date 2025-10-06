# cme-api

```json
{
  "command": "cme-api",
  "description": "CME is a utility that runs on Check Point's Security Management Server and Multi-Domain Servers running Gaia OS. CME allows cloud native integration between Check Point CloudGuard Network solutions and Cloud platforms. For more information, see the CME Administration Guide. This Management API allow you to control and configure the CME utility that is deployed on the Management Server. Use this format to execute CME API requests: Web Services syntax: <HTTP-Method> https://<mgmt-server>:<port>/web_api/cme-api/<cme-api-version>/<cme-command> mgmt_cli syntax: mgmt_cli cme-api/<cme-api-version>/<cme-command> --method <HTTP-Method> <HTTP-Method> - It is possible to use either POST, GET, DELETE or PUT based on the API documentation below. <cme-api-version> - Optional parameter. The specific version of CME API to use (such as 'v1'). Note: the latest version is used by default. <cme-command> - The CME API command that you want to use. For all available commands, see below. For a description of all CME API commands and versions and end-to-end examples, see the CME API Documentation in SwaggerHub. Note: CME-API is supported from CME take 139 and higher.",
  "request": {
    "url": "<HTTP-Method> https://<mgmt-server>:<port>/web_api/cme-api",
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
        "name": "payload",
        "description": "The payload of CME API request body.",
        "type": "string",
        "required": false
      }
    ]
  },
  "response": {
    "success": [
      {
        "name": "error",
        "description": "The error object of a failed call response from the CME API in json format.",
        "type": "Object",
        "required": false
      },
      {
        "name": "result",
        "description": "The result object of a successful call response from the CME API in json format.",
        "type": "Object",
        "required": false
      },
      {
        "name": "status-code",
        "description": "HTTP status code of a response from the CME API.",
        "type": "integer",
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
    "Add a new account (Previously known as \"Controller\")": {
      "description": "",
      "request": "POST {{server}}/v1.8/cme-api/v1/accounts/azure\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"azure_unique_name\",\n  \"subscription\" : \"12341234-1234-1234-1234-123412341234\",\n  \"application_id\" : \"56785678-5678-5678-5678-567856785678\",\n  \"directory_id\" : \"abcdabcd-abcd-abcd-abcd-abcdabcdabcd\",\n  \"client_secret\" : \"1234\"\n}",
      "response": "{\n  \"status-code\" : 200,\n  \"result\" : { },\n  \"error\" : { }\n}"
    },
    "Add a new Azure GW configuration (Previously known as \"Template\")": {
      "description": "",
      "request": "POST {{server}}/v1.8/cme-api/v1/gwConfigurations/azure\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"azure_gw_configuration\",\n  \"base64_sic_key\" : \"Base64SIC\",\n  \"version\" : \"R81\",\n  \"policy\" : \"Standard\",\n  \"related_account\" : \"azure_unique_name\"\n}",
      "response": "{\n  \"status-code\" : 200,\n  \"result\" : { },\n  \"error\" : { }\n}"
    },
    "Delete an account (Previously known as \"Controller\")": {
      "description": "",
      "request": "DELETE {{server}}/v1.8/cme-api/v1/accounts/azure_unique_name\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{ }",
      "response": "{\n  \"status-code\" : 200,\n  \"result\" : { },\n  \"error\" : { }\n}"
    },
    "Get CME version": {
      "description": "",
      "request": "GET {{server}}/v1.8/cme-api/v1/generalConfiguration/cmeVersion\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{ }",
      "response": "{\n  \"status-code\" : 200,\n  \"result\" : {\n    \"take\" : 139\n  },\n  \"error\" : { }\n}"
    },
    "Set CME Management name": {
      "description": "",
      "request": "PUT {{server}}/v1.8/cme-api/v1/management\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"azure_MGMT\"\n}",
      "response": "{\n  \"status-code\" : 200,\n  \"result\" : { },\n  \"error\" : { }\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:14.129795",
    "source_file": "cme-api.html"
  }
}
```