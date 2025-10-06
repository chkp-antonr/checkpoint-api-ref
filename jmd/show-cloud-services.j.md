# show-cloud-services

```json
{
  "command": "show-cloud-services",
  "description": "Show the connection status of the Management Server to Check Point's Infinity Portal.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/show-cloud-services",
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
        "name": "status",
        "description": "Status of the connection to the Infinity Portal.",
        "type": "string",
        "required": false,
        "valid_values": [
          "not connected",
          "connected",
          "disconnected",
          "disabled"
        ]
      },
      {
        "name": "connected-at",
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
        "name": "management-url",
        "description": "The Management Server's public URL.",
        "type": "string",
        "required": false
      },
      {
        "name": "tenant-id",
        "description": "Tenant ID of Infinity Portal.",
        "type": "string",
        "required": false
      },
      {
        "name": "gateways-onboarding-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "automatically",
          "after install policy"
        ]
      },
      {
        "name": "enabled",
        "description": "Enable/Disable automatic connection of Security Gateways to Infinity Portal.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "connection-method",
        "description": "Indicate whether Gateways will be connected to Infinity Portal automatically or only after policy installation.",
        "type": "string",
        "required": false,
        "valid_values": [
          "automatically",
          "after install policy"
        ]
      },
      {
        "name": "participant-gateways",
        "description": "Which Gateways will be connected to Infinity Portal.",
        "type": "string",
        "required": false,
        "valid_values": [
          "all",
          "specific"
        ]
      },
      {
        "name": "specific-gateways",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "aquamarine",
          "black",
          "blue",
          "crete blue",
          "burlywood",
          "cyan",
          "dark green",
          "khaki",
          "orchid",
          "dark orange",
          "dark sea green",
          "pink",
          "turquoise",
          "dark blue",
          "firebrick",
          "brown",
          "forest green",
          "gold",
          "dark gold",
          "gray",
          "dark gray",
          "light green",
          "lemon chiffon",
          "coral",
          "sea green",
          "sky blue",
          "magenta",
          "purple",
          "slate blue",
          "violet red",
          "navy blue",
          "olive",
          "orange",
          "red",
          "sienna",
          "yellow",
          "none"
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
        "name": "type",
        "description": "Object type.",
        "type": "string",
        "required": false
      },
      {
        "name": "color",
        "description": "Color of the object. Should be one of existing colors.",
        "type": "string",
        "required": false,
        "valid_values": [
          "aquamarine",
          "black",
          "blue",
          "crete blue",
          "burlywood",
          "cyan",
          "dark green",
          "khaki",
          "orchid",
          "dark orange",
          "dark sea green",
          "pink",
          "turquoise",
          "dark blue",
          "firebrick",
          "brown",
          "forest green",
          "gold",
          "dark gold",
          "gray",
          "dark gray",
          "light green",
          "lemon chiffon",
          "coral",
          "sea green",
          "sky blue",
          "magenta",
          "purple",
          "slate blue",
          "violet red",
          "navy blue",
          "olive",
          "orange",
          "red",
          "sienna",
          "yellow",
          "none"
        ]
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
      },
      {
        "name": "icon",
        "description": "Object icon.",
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
    "show-cloud-services": {
      "description": "Show the connection status of the management server to Check Point Smart-1 Cloud services.",
      "request": "POST {{server}}/show-cloud-services\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{ }",
      "response": "{\n  \"status\" : \"connected\",\n  \"connected-at\" : {\n    \"posix\" : 1638897548267,\n    \"iso-8601\" : \"2021-12-07T19:19+0200\"\n  },\n  \"management-url\" : \"https://web-server/app/maas/api/v2/environments/e8772cdf-303e-4e58-9afe-2390cae717c0\",\n  \"gateways-onboarding-settings\" : {\n    \"enabled\" : true,\n    \"participant-gateways\" : \"specific\",\n    \"connection-method\" : \"after install policy\",\n    \"specific-gateways\" : [ {\n      \"uid\" : \"e4b448ef-2635-40f0-ac46-11751597c6c6\",\n      \"name\" : \"gw1\",\n      \"type\" : \"simple-gateway\",\n      \"domain\" : {\n        \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n        \"name\" : \"SMC User\",\n        \"domain-type\" : \"domain\"\n      },\n      \"icon\" : \"NetworkObjects/gateway\",\n      \"color\" : \"black\"\n    } ]\n  }\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:23.312505",
    "source_file": "show-cloud-services.html"
  }
}
```