# get-interfaces

```json
{
  "command": "get-interfaces",
  "description": "Get physical interfaces with or without their topology from a Gaia Security Gateway or Cluster. Note: The fetched topology is based on static routes. Prerequisites: 1) SIC must be established in the Security Gateway or Cluster Member object. 2) Security Gateway or Cluster Members must be up and running.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/get-interfaces",
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
        "name": "target-uid",
        "description": "Target unique identifier.",
        "type": "string",
        "required": true
      },
      {
        "name": "group-interfaces-by-subnet",
        "description": "Specify whether to group the cluster interfaces by a subnet. Otherwise, group the cluster interfaces by their names.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "use-defined-by-routes",
        "description": "Specify whether to configure the topology \"Defined by Routes\" where applicable. Otherwise, configure the topology to \"This Network\" as default for internal interfaces.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "with-topology",
        "description": "Specify whether to fetch the interfaces with their topology. Otherwise, the Management Server fetches the interfaces without their topology.",
        "type": "boolean",
        "required": false,
        "default": "false"
      }
    ]
  },
  "response": {
    "success": [
      {
        "name": "task-id",
        "description": "The UID of the \"get-interfaces\" task. Use the \"show-task\" command to check the progress of the \"get-interfaces\" task.",
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
    "get-interfaces without topology by UID": {
      "description": "Get interfaces without topology from target gateway or cluster by UID",
      "request": "POST {{server}}/get-interfaces\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"target-uid\" : \"2220d9ad-a251-5555-9a0a-4772a6511111\",\n  \"with-topology\" : false\n}",
      "response": "{\n  \"tasks\" : [ {\n    \"task-name\" : \"get-interfaces\",\n    \"task-id\" : \"01234567-89ab-cdef-9e1f-0e1e68312345\",\n    \"status\" : \"succeeded\",\n    \"progress-percentage\" : 100,\n    \"suppressed\" : false,\n    \"task-details\" : [ {\n      \"interfaces\" : [ \"eth0\", \"eth1\" ]\n    } ]\n  } ]\n}"
    },
    "get-interfaces with topology by name": {
      "description": "Get interfaces with topology from target gateway or cluster by name",
      "request": "POST {{server}}/get-interfaces\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"target-name\" : \"gw123\",\n  \"with-topology\" : true\n}",
      "response": "{\n  \"tasks\" : [ {\n    \"task-name\" : \"get-interfaces\",\n    \"task-id\" : \"01234567-89ab-cdef-9e1f-0e1e68312345\",\n    \"status\" : \"succeeded\",\n    \"progress-percentage\" : 100,\n    \"suppressed\" : false,\n    \"task-details\" : [ {\n      \"interfaces\" : [ \"eth0\", \"eth1\" ]\n    } ]\n  } ]\n}"
    },
    "get-interfaces with topology by name, more than 50 interfaces returned": {
      "description": "Get physical interfaces with or without their topology from a Gaia Security Gateway or Cluster that is specified by its object name and contains more than 50 interfaces. Note: The response contains only the first 50 interfaces and the total number of interfaces in the object.",
      "request": "POST {{server}}/get-interfaces\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"target-name\" : \"gw123\",\n  \"with-topology\" : true\n}",
      "response": "{\n  \"tasks\" : [ {\n    \"task-name\" : \"get-interfaces\",\n    \"task-id\" : \"01234567-89ab-cdef-9e1f-0e1e68312345\",\n    \"status\" : \"succeeded\",\n    \"progress-percentage\" : 100,\n    \"suppressed\" : false,\n    \"task-details\" : [ {\n      \"interfaces\" : [ \"eth0\", \"eth1\", \"...\", \"eth49\" ],\n      \"total\" : 85\n    } ]\n  } ]\n}"
    },
    "get-interfaces with topology by name don't use Defined by Routes": {
      "description": "Get interfaces with topology from target gateway or cluster by name, don't use Defined by Routes topology",
      "request": "POST {{server}}/get-interfaces\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"target-name\" : \"gw123\",\n  \"with-topology\" : true,\n  \"use-defined-by-routes\" : false\n}",
      "response": "{\n  \"tasks\" : [ {\n    \"task-name\" : \"get-interfaces\",\n    \"task-id\" : \"01234567-89ab-cdef-9e1f-0e1e68312345\",\n    \"status\" : \"succeeded\",\n    \"progress-percentage\" : 100,\n    \"suppressed\" : false,\n    \"task-details\" : [ {\n      \"interfaces\" : [ \"eth0\", \"eth1\" ]\n    } ]\n  } ]\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:15.414967",
    "source_file": "get-interfaces.html"
  }
}
```