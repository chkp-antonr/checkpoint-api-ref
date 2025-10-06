# set-securemote-dns-server

```json
{
  "command": "set-securemote-dns-server",
  "description": "Edit existing SecuRemote DNS server using object name or uid.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/set-securemote-dns-server",
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
        "name": "new-name",
        "description": "New name of the object.",
        "type": "string",
        "required": false
      },
      {
        "name": "host",
        "description": "DNS server for remote clients in the Remote access community. Identified by name or UID.",
        "type": "string",
        "required": false
      },
      {
        "name": "domains",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "add",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "domain-suffix",
        "description": "DNS Domain suffix.",
        "type": "string",
        "required": true
      },
      {
        "name": "maximum-prefix-label-count",
        "description": "Maximum number of matching labels preceding the suffix.",
        "type": "integerDescription:",
        "required": false
      },
      {
        "name": "domain-suffix",
        "description": "DNS Domain suffix.",
        "type": "string",
        "required": true
      },
      {
        "name": "maximum-prefix-label-count",
        "description": "Maximum number of matching labels preceding the suffix.",
        "type": "integerDescription:",
        "required": false
      },
      {
        "name": "remove",
        "description": "Removes from collection of values",
        "type": "string",
        "required": false
      },
      {
        "name": "update",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "domain-suffix",
        "description": "DNS Domain suffix.",
        "type": "string",
        "required": true
      },
      {
        "name": "maximum-prefix-label-count",
        "description": "Maximum number of matching labels preceding the suffix.",
        "type": "integerDescription:",
        "required": false
      },
      {
        "name": "new-domain-suffix",
        "description": "New DNS Domain suffix.",
        "type": "string",
        "required": false
      },
      {
        "name": "domain-suffix",
        "description": "DNS Domain suffix.",
        "type": "string",
        "required": true
      },
      {
        "name": "maximum-prefix-label-count",
        "description": "Maximum number of matching labels preceding the suffix.",
        "type": "integerDescription:",
        "required": false
      },
      {
        "name": "domain-suffix",
        "description": "DNS Domain suffix.",
        "type": "string",
        "required": true
      },
      {
        "name": "maximum-prefix-label-count",
        "description": "Maximum number of matching labels preceding the suffix.",
        "type": "integerDescription:",
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
        "name": "host",
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
      },
      {
        "name": "domains",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "domain-suffix",
        "description": "DNS Domain suffix.",
        "type": "string",
        "required": false
      },
      {
        "name": "maximum-prefix-label-count",
        "description": "Maximum number of matching labels preceding the suffix.",
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
    "set securemote-dns-server": {
      "description": "Edits SecuRemote DNS server.",
      "request": "POST {{server}}/set-securemote-dns-server\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"TestSecuRemoteDNSSever\",\n  \"host\" : \"TestHost2\",\n  \"domains\" : {\n    \"domain-suffix\" : \".ThirdDomain\",\n    \"maximum-prefix-label-count\" : 2\n  }\n}",
      "response": "{\n  \"uid\" : \"2851178b-d315-4687-b48d-eb45b656e14f\",\n  \"name\" : \"TestSecuRemoteDNSSever\",\n  \"type\" : \"securemote-dns-server\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1746457943976,\n      \"iso-8601\" : \"2025-05-05T18:12+0300\"\n    },\n    \"last-modifier\" : \"WEB_API\",\n    \"creation-time\" : {\n      \"posix\" : 1746457746967,\n      \"iso-8601\" : \"2025-05-05T18:09+0300\"\n    },\n    \"creator\" : \"WEB_API\"\n  },\n  \"available-actions\" : { },\n  \"tags\" : [ ],\n  \"read-only\" : true,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"Objects/account_unit\",\n  \"host\" : {\n    \"uid\" : \"0ee12048-a8d3-4a11-9fd9-89825785b20b\",\n    \"name\" : \"TestHost2\",\n    \"type\" : \"host\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"icon\" : \"Objects/host\",\n    \"color\" : \"black\",\n    \"ipv4-address\" : \"2.2.2.2\"\n  },\n  \"domains\" : [ {\n    \"domain-suffix\" : \".ThirdDomain\",\n    \"maximum-prefix-label-count\" : 2\n  } ]\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:19.078318",
    "source_file": "set-securemote-dns-server.html"
  }
}
```