# set-data-type-weighted-keywords

```json
{
  "command": "set-data-type-weighted-keywords",
  "description": "Edit existing Weighted Keywords Data Type object using object name or uid.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/set-data-type-weighted-keywords",
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
        "name": "description",
        "description": "For built-in data types, the description explains the purpose of this type of data representation. For custom-made data types, you can use this field to provide more details.",
        "type": "string",
        "required": false
      },
      {
        "name": "weighted-keywords",
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
        "name": "keyword",
        "description": "keyword or regular expression to be weighted.",
        "type": "string",
        "required": true
      },
      {
        "name": "weight",
        "description": "Weight of the expression.",
        "type": "integer",
        "required": false
      },
      {
        "name": "max-weight",
        "description": "Max weight of the expression.",
        "type": "integer",
        "required": false
      },
      {
        "name": "regex",
        "description": "Determine whether to consider the expression as a regular expression.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "keyword",
        "description": "keyword or regular expression to be weighted.",
        "type": "string",
        "required": true
      },
      {
        "name": "weight",
        "description": "Weight of the expression.",
        "type": "integer",
        "required": false
      },
      {
        "name": "max-weight",
        "description": "Max weight of the expression.",
        "type": "integer",
        "required": false
      },
      {
        "name": "regex",
        "description": "Determine whether to consider the expression as a regular expression.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "remove",
        "description": "Removes from collection of values",
        "type": "string",
        "required": false
      },
      {
        "name": "keyword",
        "description": "keyword or regular expression to be weighted.",
        "type": "string",
        "required": true
      },
      {
        "name": "weight",
        "description": "Weight of the expression.",
        "type": "integer",
        "required": false
      },
      {
        "name": "max-weight",
        "description": "Max weight of the expression.",
        "type": "integer",
        "required": false
      },
      {
        "name": "regex",
        "description": "Determine whether to consider the expression as a regular expression.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "keyword",
        "description": "keyword or regular expression to be weighted.",
        "type": "string",
        "required": true
      },
      {
        "name": "weight",
        "description": "Weight of the expression.",
        "type": "integer",
        "required": false
      },
      {
        "name": "max-weight",
        "description": "Max weight of the expression.",
        "type": "integer",
        "required": false
      },
      {
        "name": "regex",
        "description": "Determine whether to consider the expression as a regular expression.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "sum-of-weights-threshold",
        "description": "Define the number of appearances, by weight, of all the keywords that, beyond this threshold, the data containing this list of words or phrases will be recognized as data to be protected.",
        "type": "integer",
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
        "name": "description",
        "description": "For built-in data types, the description explains the purpose of this type of data representation. For custom-made data types, you can use this field to provide more details.",
        "type": "string",
        "required": false
      },
      {
        "name": "weighted-keywords",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "keyword",
        "description": "keyword or regular expression to be weighted.",
        "type": "string",
        "required": false
      },
      {
        "name": "weight",
        "description": "weight of the expression.",
        "type": "integer",
        "required": false
      },
      {
        "name": "max-weight",
        "description": "max weight of the expression.",
        "type": "integer",
        "required": false
      },
      {
        "name": "regex",
        "description": "Determine weather to consider the expression as a regular expression.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "sum-of-weights-threshold",
        "description": "Define the number of appearances, by weight, of all the keywords that, beyond this threshold, the data containing this list of words or phrases will be recognized as data to be protected.",
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
    "show-data-type-weighted-keywords": {
      "description": "",
      "request": "POST {{server}}/show-data-type-weighted-keywords\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"weighted-words-obj\",\n  \"weighted-keywords.add.1.keyword\" : \"word2\",\n  \"weighted-keywords.add.1.weight\" : 2,\n  \"weighted-keywords.add.1.max-weight\" : 4,\n  \"weighted-keywords.add.1.regex\" : false,\n  \"sum-of-weights-threshold\" : 15\n}",
      "response": "{\n  \"uid\" : \"e9ddaf70-2694-49f7-b092-e068d4ecc32c\",\n  \"name\" : \"weighted-words-obj\",\n  \"type\" : \"data-type-weighted-keywords\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1695674282632,\n      \"iso-8601\" : \"2023-09-25T23:38+0300\"\n    },\n    \"last-modifier\" : \"WEB_API\",\n    \"creation-time\" : {\n      \"posix\" : 1695673743465,\n      \"iso-8601\" : \"2023-09-25T23:29+0300\"\n    },\n    \"creator\" : \"WEB_API\"\n  },\n  \"available-actions\" : { },\n  \"tags\" : [ ],\n  \"read-only\" : true,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"DataLossPrevention/Data_Object\",\n  \"weighted-keywords\" : [ {\n    \"keyword\" : \"word1\",\n    \"weight\" : 3,\n    \"max-weight\" : 4,\n    \"regex\" : true\n  }, {\n    \"keyword\" : \"word2\",\n    \"weight\" : 2,\n    \"max-weight\" : 4,\n    \"regex\" : true\n  } ],\n  \"sum-of-weights-threshold\" : 15\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:16.535600",
    "source_file": "set-data-type-weighted-keywords.html"
  }
}
```