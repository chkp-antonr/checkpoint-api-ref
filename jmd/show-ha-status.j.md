# show-ha-status

```json
{
  "command": "show-ha-status",
  "description": "Retrieve domain high availability status.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/show-ha-status",
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
          "domain",
          "global domain",
          "mds"
        ]
      },
      {
        "name": "servers",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "active",
          "standby"
        ]
      },
      {
        "name": "name",
        "description": "Object name. Must be unique in the domain.",
        "type": "string",
        "required": false
      },
      {
        "name": "ip-address",
        "description": "Server IPv4 or IPv6 address.",
        "type": "string",
        "required": false
      },
      {
        "name": "ha-state",
        "description": "High availability state.",
        "type": "string",
        "required": false,
        "valid_values": [
          "active",
          "standby"
        ]
      },
      {
        "name": "last-successful-sync",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "iso-8601",
        "description": "Date and time represented in international ISO 8601 format.",
        "type": "string",
        "required": false
      },
      {
        "name": "posix",
        "description": "Number of milliseconds that have elapsed since 00:00:00, 1 January 1970.",
        "type": "integer",
        "required": false
      },
      {
        "name": "sync-state",
        "description": "Sync State - shown only for standby peers.",
        "type": "string",
        "required": false,
        "valid_values": [
          "Ok",
          "Communication Error",
          "Sync Error"
        ]
      },
      {
        "name": "multi-domain-server",
        "description": "Multi Domain server name.",
        "type": "string",
        "required": false
      },
      {
        "name": "successfully-synced",
        "description": "The HA status of the domain.",
        "type": "boolean",
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
    "show ha status from local domain": {
      "description": "Shows HA sync status called from local active domain.",
      "request": "POST {{server}}/show-ha-status\nContent-type: application/json\nX-chkp-sid: {{session}}\n\n{ }",
      "response": "{\n  \"uid\" : \"041ca0c2-c15f-4a70-8116-02933383bffb\",\n  \"name\" : \"domain1\",\n  \"domain-type\" : \"domain\",\n  \"servers\" : [ {\n    \"ip-address\" : \"172.23.3.234\",\n    \"ha-state\" : \"standby\",\n    \"multi-domain-server\" : \"secondary\",\n    \"last-successful-sync\" : {\n      \"posix\" : 1672146619056,\n      \"iso-8601\" : \"2022-12-27T15:10+0200\"\n    },\n    \"sync-state\" : \"Ok\"\n  }, {\n    \"ip-address\" : \"172.23.3.235\",\n    \"ha-state\" : \"standby\",\n    \"multi-domain-server\" : \"secondary2\",\n    \"sync-state\" : \"Sync Error\"\n  } ],\n  \"successfully-synced\" : false\n}"
    },
    "show ha status from system domain": {
      "description": "Shows HA sync status called from system domain.",
      "request": "POST {{server}}/show-ha-status\nContent-type: application/json\nX-chkp-sid: {{session}}\n\n{ }",
      "response": "{\n  \"uid\" : \"a0eebc99-afed-4ef8-bb6d-fedfedfedfed\",\n  \"name\" : \"System Data\",\n  \"domain-type\" : \"mds\",\n  \"successfully-synced\" : true\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:24.980638",
    "source_file": "show-ha-status.html"
  }
}
```