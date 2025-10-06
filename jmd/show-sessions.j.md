# show-sessions

```json
{
  "command": "show-sessions",
  "description": "Retrieve all objects.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/show-sessions",
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
        "name": "filter",
        "description": "Search expression to filter objects by. The provided text should be exactly the same as it would be given in SmartConsole Object Explorer. The logical operators in the expression ('AND', 'OR') should be provided in capital letters. The search involves both a IP search and a textual search in name, comment, tags etc.",
        "type": "string",
        "required": false
      },
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
      },
      {
        "name": "view-published-sessions",
        "description": "Show a list of published sessions.",
        "type": "boolean",
        "required": false,
        "default": "false"
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
    "show-sessions": {
      "description": "Show all the sessions. Details level: UID",
      "request": "POST {{server}}/show-sessions\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"limit\" : 50,\n  \"offset\" : 0,\n  \"details-level\" : \"standard\"\n}",
      "response": "{\n  \"from\" : 1,\n  \"to\" : 16,\n  \"total\" : 16,\n  \"objects\" : [ \"01f83a11-179a-405a-971a-50c58368f415\", \"27aabb7e-263a-4161-b822-0e0078c72e06\", \"2b486864-1356-4b66-ae6b-6eda09821955\", \"3f457555-01af-49ce-a3e9-4c62432c7777\", \"68d44bae-30b8-4348-b875-ef11ae216286\", \"9c8345cc-50b9-466e-a608-cfcf03e7b567\", \"9fc9aa4a-8e16-4c34-a951-5c80799dd270\", \"a6b8c425-33b0-4b4d-914b-9f1813c423e0\", \"b1ddc72d-d668-4a6b-8f08-1b4b75c372ab\", \"bc2abbca-61a6-460d-9b48-b429c27dcc15\", \"c0377672-b7b1-43ce-afdd-5d14adfe68ca\", \"ce35609f-050d-4a21-a138-23063831ed68\", \"e71080c0-edc8-4c98-9f17-72c5855961b6\", \"eab7f3e2-c06f-4c5f-9e3a-175e8d7357d4\", \"fe5936ff-8812-4716-8d87-939e855791f8\", \"ffc5d5a3-6def-474c-b75c-d2a685b45905\" ]\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:27.837413",
    "source_file": "show-sessions.html"
  }
}
```