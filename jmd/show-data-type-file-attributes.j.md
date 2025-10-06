# show-data-type-file-attributes

```json
{
  "command": "show-data-type-file-attributes",
  "description": "Retrieve existing File Attributes Data Type object using object name or uid.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/show-data-type-file-attributes",
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
        "name": "description",
        "description": "For built-in data types, the description explains the purpose of this type of data representation. For custom-made data types, you can use this field to provide more details.",
        "type": "string",
        "required": false
      },
      {
        "name": "match-by-file-type",
        "description": "Determine whether to consider file type.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "file-groups-list",
        "description": "",
        "type": "array",
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
        "name": "match-by-file-name",
        "description": "Determine whether to consider file name.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "file-name-contains",
        "description": "File name should contain the expression.",
        "type": "string",
        "required": false
      },
      {
        "name": "match-by-file-size",
        "description": "Determine whether to consider file size.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "file-size",
        "description": "Min File size in KB.",
        "type": "integer",
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
    "show-data-type-file-attributes": {
      "description": "",
      "request": "POST {{server}}/show-data-type-file-attributes\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"file-attr-obj\"\n}",
      "response": "{\n  \"uid\" : \"b3f18062-57c4-43f9-b3d4-6aed11c8c688\",\n  \"name\" : \"file-attr-obj\",\n  \"type\" : \"data-type-file-attributes\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1695670212542,\n      \"iso-8601\" : \"2023-09-25T22:30+0300\"\n    },\n    \"last-modifier\" : \"WEB_API\",\n    \"creation-time\" : {\n      \"posix\" : 1695670212542,\n      \"iso-8601\" : \"2023-09-25T22:30+0300\"\n    },\n    \"creator\" : \"WEB_API\"\n  },\n  \"available-actions\" : {\n    \"edit\" : \"true\",\n    \"delete\" : \"true\",\n    \"clone\" : \"false\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : false,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"DataLossPrevention/Data_Object\",\n  \"match-by-file-size\" : true,\n  \"match-by-file-name\" : true,\n  \"match-by-file-type\" : true,\n  \"file-size\" : 14,\n  \"file-name-contains\" : \"expression\",\n  \"file-groups-list\" : [ {\n    \"uid\" : \"5d14b031-f3a9-431b-82a6-9f5e1bca77e8\",\n    \"name\" : \"Viewer\",\n    \"type\" : \"data-type-file-group\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"icon\" : \"DataLossPrevention/viewer_group\",\n    \"color\" : \"black\"\n  } ]\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:23.761880",
    "source_file": "show-data-type-file-attributes.html"
  }
}
```