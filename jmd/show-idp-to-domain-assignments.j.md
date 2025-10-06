# show-idp-to-domain-assignments

```json
{
  "command": "show-idp-to-domain-assignments",
  "description": "Retrieve all Identity Provider to domain assignments. This command only available for Multi-Domain server.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/show-idp-to-domain-assignments",
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
        "name": "from",
        "description": "From which element number the query was done.",
        "type": "integer",
        "required": false
      },
      {
        "name": "objects",
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
        "name": "to",
        "description": "To which element number the query was done.",
        "type": "integer",
        "required": false
      },
      {
        "name": "total",
        "description": "Total number of elements returned by the query.",
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
    "show all idp-to-domain-assignments objects": {
      "description": "show all idp-to-domain-assignments objects",
      "request": "POST {{server}}/show-idp-to-domain-assignments\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"details-level\" : \"full\"\n}\n\n \u2022 This command is available only after logging in to the System Data domain.",
      "response": "{\n  \"from\" : 1,\n  \"to\" : 2,\n  \"total\" : -1,\n  \"objects\" : [ {\n    \"uid\" : \"fe866287-248a-4fb3-9e5e-bb0e1ac90788\",\n    \"type\" : \"idp-to-domain-assignment\",\n    \"domain\" : {\n      \"uid\" : \"a0eebc99-afed-4ef8-bb6d-fedfedfedfed\",\n      \"name\" : \"System Data\",\n      \"domain-type\" : \"mds\"\n    },\n    \"meta-info\" : {\n      \"lock\" : \"unlocked\",\n      \"validation-state\" : \"ok\",\n      \"last-modify-time\" : {\n        \"posix\" : 1642077724898,\n        \"iso-8601\" : \"2022-01-13T14:42+0200\"\n      },\n      \"last-modifier\" : \"WEB_API\",\n      \"creation-time\" : {\n        \"posix\" : 1641462834333,\n        \"iso-8601\" : \"2022-01-06T11:53+0200\"\n      },\n      \"creator\" : \"System\"\n    },\n    \"tags\" : [ ],\n    \"read-only\" : false,\n    \"identity-provider-set\" : false,\n    \"using-default\" : true,\n    \"assigned-domain\" : {\n      \"uid\" : \"e6e6cc24-9881-4869-975c-7b3ac8d4347d\",\n      \"name\" : \"BSMS\",\n      \"type\" : \"domain\",\n      \"domain\" : {\n        \"uid\" : \"a0eebc99-afed-4ef8-bb6d-fedfedfedfed\",\n        \"name\" : \"System Data\",\n        \"domain-type\" : \"mds\"\n      },\n      \"meta-info\" : {\n        \"lock\" : \"unlocked\",\n        \"validation-state\" : \"ok\",\n        \"last-modify-time\" : {\n          \"posix\" : 1641463212554,\n          \"iso-8601\" : \"2022-01-06T12:00+0200\"\n        },\n        \"last-modifier\" : \"System\",\n        \"creation-time\" : {\n          \"posix\" : 1641462830597,\n          \"iso-8601\" : \"2022-01-06T11:53+0200\"\n        },\n        \"creator\" : \"aa\"\n      },\n      \"tags\" : [ ],\n      \"read-only\" : false,\n      \"comments\" : \"\",\n      \"color\" : \"black\",\n      \"icon\" : \"Objects/domain\",\n      \"domain-type\" : \"domain\",\n      \"servers\" : [ {\n        \"name\" : \"BSMS_Server\",\n        \"type\" : \"management server\",\n        \"ipv4-address\" : \"172.28.2.121\",\n        \"multi-domain-server\" : \"Firewall-ivory-main-take-263\",\n        \"active\" : true\n      } ],\n      \"global-domain-assignments\" : [ ]\n    }\n  }, {\n    \"uid\" : \"2feed858-373b-4618-ae03-84e1a08bad72\",\n    \"type\" : \"idp-to-domain-assignment\",\n    \"domain\" : {\n      \"uid\" : \"a0eebc99-afed-4ef8-bb6d-fedfedfedfed\",\n      \"name\" : \"System Data\",\n      \"domain-type\" : \"mds\"\n    },\n    \"meta-info\" : {\n      \"lock\" : \"unlocked\",\n      \"validation-state\" : \"ok\",\n      \"last-modify-time\" : {\n        \"posix\" : 1642078321824,\n        \"iso-8601\" : \"2022-01-13T14:52+0200\"\n      },\n      \"last-modifier\" : \"aa\",\n      \"creation-time\" : {\n        \"posix\" : 1641229065206,\n        \"iso-8601\" : \"2022-01-03T18:57+0200\"\n      },\n      \"creator\" : \"System\"\n    },\n    \"tags\" : [ ],\n    \"read-only\" : false,\n    \"identity-provider-set\" : false,\n    \"using-default\" : true,\n    \"assigned-domain\" : {\n      \"uid\" : \"8ecf2426-268d-44c6-95c6-85289d34318f\",\n      \"name\" : \"SMS\",\n      \"type\" : \"domain\",\n      \"domain\" : {\n        \"uid\" : \"a0eebc99-afed-4ef8-bb6d-fedfedfedfed\",\n        \"name\" : \"System Data\",\n        \"domain-type\" : \"mds\"\n      },\n      \"meta-info\" : {\n        \"lock\" : \"unlocked\",\n        \"validation-state\" : \"ok\",\n        \"last-modify-time\" : {\n          \"posix\" : 1641229402073,\n          \"iso-8601\" : \"2022-01-03T19:03+0200\"\n        },\n        \"last-modifier\" : \"arig@checkpoint.com\",\n        \"creation-time\" : {\n          \"posix\" : 1641229063850,\n          \"iso-8601\" : \"2022-01-03T18:57+0200\"\n        },\n        \"creator\" : \"Remote CPM Server\"\n      },\n      \"tags\" : [ ],\n      \"read-only\" : false,\n      \"comments\" : \"\",\n      \"color\" : \"black\",\n      \"icon\" : \"Objects/domain\",\n      \"domain-type\" : \"domain\",\n      \"servers\" : [ {\n        \"name\" : \"SMS_Server\",\n        \"type\" : \"management server\",\n        \"ipv4-address\" : \"172.28.2.194\",\n        \"multi-domain-server\" : \"Firewall-ivory-main-take-263\",\n        \"active\" : true\n      }, {\n        \"name\" : \"SMS_Server_2\",\n        \"type\" : \"management server\",\n        \"ipv4-address\" : \"172.28.2.196\",\n        \"multi-domain-server\" : \"site-b\",\n        \"active\" : false\n      } ],\n      \"global-domain-assignments\" : [ ]\n    }\n  } ]\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:25.384733",
    "source_file": "show-idp-to-domain-assignments.html"
  }
}
```