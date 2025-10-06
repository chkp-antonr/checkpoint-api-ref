# show-repository-packages

```json
{
  "command": "show-repository-packages",
  "description": "Gets all repository software packages information.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/show-repository-packages",
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
        "name": "limit",
        "description": "The maximal number of returned results.",
        "type": "integer",
        "required": false,
        "default": "50"
      },
      {
        "name": "offset",
        "description": "Number of the results to initially skip.",
        "type": "integer",
        "required": false,
        "default": "0"
      },
      {
        "name": "order",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "name"
        ]
      },
      {
        "name": "ASC",
        "description": "Sorts results by the given field in ascending order.",
        "type": "string",
        "required": false,
        "valid_values": [
          "name"
        ]
      }
    ]
  },
  "response": {
    "success": [
      {
        "name": "task-id",
        "description": "Unique identifier of the 'show-repository-packages' task. Use the 'show-task' command to check the progress of the task.",
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
    "show-repository-packages": {
      "description": "",
      "request": "POST {{server}}/show-repository-packages\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"limit\" : 50,\n  \"offset\" : 0,\n  \"details-level\" : \"standard\"\n}",
      "response": "{\n  \"tasks\" : [ {\n    \"uid\" : \"f6241fa3-1bca-45a9-a700-968bde6c7219\",\n    \"type\" : \"task\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"meta-info\" : {\n      \"lock\" : \"unlocked\",\n      \"validation-state\" : \"ok\",\n      \"last-modify-time\" : {\n        \"posix\" : 1588785254969,\n        \"iso-8601\" : \"2020-05-06T20:14+0300\"\n      },\n      \"last-modifier\" : \"WEB_API\",\n      \"creation-time\" : {\n        \"posix\" : 1588785254029,\n        \"iso-8601\" : \"2020-05-06T20:14+0300\"\n      },\n      \"creator\" : \"WEB_API\"\n    },\n    \"tags\" : [ ],\n    \"read-only\" : false,\n    \"comments\" : \"\",\n    \"color\" : \"black\",\n    \"icon\" : \"General/globalsNa\",\n    \"task-name\" : \"Getting information for this software package:all\",\n    \"task-id\" : \"bdfd4078-8344-4468-b41e-dd3bc70e6da9\",\n    \"status\" : \"succeeded\",\n    \"progress-percentage\" : 100,\n    \"start-time\" : {\n      \"posix\" : 1588785254018,\n      \"iso-8601\" : \"2020-05-06T20:14+0300\"\n    },\n    \"last-update-time\" : {\n      \"posix\" : 1588785254958,\n      \"iso-8601\" : \"2020-05-06T20:14+0300\"\n    },\n    \"suppressed\" : true,\n    \"task-details\" : [ {\n      \"uid\" : \"00189172-c7b3-40c0-ace2-ec14067d63d5\",\n      \"name\" : null,\n      \"domain\" : {\n        \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n        \"name\" : \"SMC User\",\n        \"domain-type\" : \"domain\"\n      },\n      \"color\" : \"black\",\n      \"statusDescription\" : \"\",\n      \"taskNotification\" : \"f6241fa3-1bca-45a9-a700-968bde6c7219\",\n      \"meta-info\" : {\n        \"validation-state\" : \"ok\",\n        \"last-modify-time\" : {\n          \"posix\" : 1588785254882,\n          \"iso-8601\" : \"2020-05-06T20:14+0300\"\n        },\n        \"last-modifier\" : \"WEB_API\",\n        \"creation-time\" : {\n          \"posix\" : 1588785254882,\n          \"iso-8601\" : \"2020-05-06T20:14+0300\"\n        },\n        \"creator\" : \"WEB_API\"\n      },\n      \"tags\" : [ ],\n      \"icon\" : \"General/globalsNa\",\n      \"comments\" : \"\",\n      \"display-name\" : \"\",\n      \"customFields\" : null,\n      \"packages\" : [ {\n        \"category\" : \"hotfix\",\n        \"baseVersion\" : \"R80.20\",\n        \"name\" : \"Check_Point_R80_20_JUMBO_HF_Bundle_T118_sk137592_Security_Gateway_and_Standalone_2_6_18_FULL.tgz\",\n        \"size\" : \"792422769\",\n        \"releaseDate\" : \"2019-10-27 00:00:00\",\n        \"description\" : {\n          \"text\" : \"R80.20 Jumbo Hotfix Accumulator \u00a0General availability (Take 118). This package is suitable for Security Gateway and Standalone Gaia 2.6.18 machines only.\u00a0\",\n          \"links\" : [ ]\n        },\n        \"availability\" : \"both\"\n      }, {\n        \"category\" : \"hotfix\",\n        \"baseVersion\" : \"R80.10\",\n        \"name\" : \"Check_Point_R80_10_JUMBO_HF_Bundle_T259_FULL.tgz\",\n        \"size\" : \"864819325\",\n        \"releaseDate\" : \"\",\n        \"description\" : { },\n        \"availability\" : \"local\"\n      } ]\n    } ]\n  } ]\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:26.950006",
    "source_file": "show-repository-packages.html"
  }
}
```