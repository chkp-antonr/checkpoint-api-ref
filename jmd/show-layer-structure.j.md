# show-layer-structure

```json
{
  "command": "show-layer-structure",
  "description": "Shows the entire layer structure. The layer structure is divided into sections and each section has its own entities.Supported layer types: Access Control, NAT, Custom Threat Prevention, Threat Exception and HTTPS Inspection.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/show-layer-structure",
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
        "name": "name",
        "description": "Object name. Must be unique in the domain.",
        "type": "string",
        "required": true
      },
      {
        "name": "package",
        "description": "Name of the package. Must be set when want to receive the resolved rule instead of the place holder in global domain layer.",
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
        "name": "root-section",
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
        "name": "uid",
        "description": "Object unique identifier.",
        "type": "string",
        "required": false
      },
      {
        "name": "children",
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
        "name": "children",
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
        "description": "Object name.",
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
        "name": "rule-number",
        "description": "Rule number.",
        "type": "integer",
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
        "name": "from-rule",
        "description": "From rule. This field is relevant only for section.",
        "type": "integer",
        "required": false
      },
      {
        "name": "to-rule",
        "description": "To rule. This field is relevant only for section.",
        "type": "integer",
        "required": false
      },
      {
        "name": "tags",
        "description": "Collection of tag objects identified by the name or UID.",
        "type": "array",
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
        "name": "comments",
        "description": "Comments string.",
        "type": "string",
        "required": false
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
        "name": "meta-info",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "unlocked",
          "locked by current session",
          "locked by other session",
          "prevented by current session",
          "prevented by other session"
        ]
      },
      {
        "name": "creation-time",
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
        "name": "creator",
        "description": "N/A",
        "type": "string",
        "required": false
      },
      {
        "name": "last-modifier",
        "description": "N/A",
        "type": "string",
        "required": false
      },
      {
        "name": "last-modify-time",
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
        "name": "lock",
        "description": "Object lock state. It's not allowed to edit objects locked by other session.",
        "type": "string",
        "required": false,
        "valid_values": [
          "unlocked",
          "locked by current session",
          "locked by other session",
          "prevented by current session",
          "prevented by other session"
        ]
      },
      {
        "name": "locking-admin",
        "description": "in case the object is locked by another session it will show the administrator name that locked the object.",
        "type": "string",
        "required": false
      },
      {
        "name": "locking-session-id",
        "description": "in case the object is locked by another session it will show the session uid that locked the object.",
        "type": "string",
        "required": false
      },
      {
        "name": "validation-state",
        "description": "N/A",
        "type": "string",
        "required": false,
        "valid_values": [
          "ok",
          "info",
          "warning",
          "error"
        ]
      },
      {
        "name": "read-only",
        "description": "Indicates whether the object is read-only.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "available-actions",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "true",
          "false",
          "not_supported"
        ]
      },
      {
        "name": "clone",
        "description": "Whether you can clone the object.",
        "type": "string",
        "required": false,
        "valid_values": [
          "true",
          "false",
          "not_supported"
        ]
      },
      {
        "name": "delete",
        "description": "Whether you can delete the object.",
        "type": "string",
        "required": false,
        "valid_values": [
          "true",
          "false",
          "not_supported"
        ]
      },
      {
        "name": "edit",
        "description": "Whether you can edit the object.",
        "type": "string",
        "required": false,
        "valid_values": [
          "true",
          "false",
          "not_supported"
        ]
      },
      {
        "name": "meta-info",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "unlocked",
          "locked by current session",
          "locked by other session",
          "prevented by current session",
          "prevented by other session"
        ]
      },
      {
        "name": "creation-time",
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
        "name": "creator",
        "description": "N/A",
        "type": "string",
        "required": false
      },
      {
        "name": "last-modifier",
        "description": "N/A",
        "type": "string",
        "required": false
      },
      {
        "name": "last-modify-time",
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
        "name": "lock",
        "description": "Object lock state. It's not allowed to edit objects locked by other session.",
        "type": "string",
        "required": false,
        "valid_values": [
          "unlocked",
          "locked by current session",
          "locked by other session",
          "prevented by current session",
          "prevented by other session"
        ]
      },
      {
        "name": "locking-admin",
        "description": "in case the object is locked by another session it will show the administrator name that locked the object.",
        "type": "string",
        "required": false
      },
      {
        "name": "locking-session-id",
        "description": "in case the object is locked by another session it will show the session uid that locked the object.",
        "type": "string",
        "required": false
      },
      {
        "name": "validation-state",
        "description": "N/A",
        "type": "string",
        "required": false,
        "valid_values": [
          "ok",
          "info",
          "warning",
          "error"
        ]
      },
      {
        "name": "place-holder",
        "description": "Place holder unique identifier. This field is relevant on Multi Domain environments with global domain assignment. See 'show-place-holder' command.",
        "type": "string",
        "required": false
      },
      {
        "name": "from",
        "description": "From which element number the query was done.",
        "type": "integer",
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
    "show-layer-structure": {
      "description": "",
      "request": "POST {{server}}/show-layer-structure\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"offset\" : 0,\n  \"limit\" : 20,\n  \"name\" : \"Network\",\n  \"details-level\" : \"standard\"\n}",
      "response": "{\n  \"uid\" : \"9a6fee48-7629-431f-98c0-11ff58a6777c\",\n  \"name\" : \"Network\",\n  \"type\" : \"access-layer\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"from\" : 1,\n  \"to\" : 5,\n  \"total\" : 5,\n  \"root-section\" : {\n    \"uid\" : \"35052cc0-3eca-4a5c-abcc-84f352d19aa1\",\n    \"children\" : [ {\n      \"uid\" : \"2c60825c-d5d0-44f4-952a-6b34a0bfb018\",\n      \"name\" : \"rule 1\",\n      \"type\" : \"access-rule\",\n      \"domain\" : {\n        \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n        \"name\" : \"SMC User\",\n        \"domain-type\" : \"domain\"\n      },\n      \"icon\" : \"Objects/accessRule\",\n      \"color\" : \"black\",\n      \"rule-number\" : 1\n    }, {\n      \"uid\" : \"d38fd152-8f18-4769-91d2-00207ec15ece\",\n      \"name\" : \"rule 2\",\n      \"type\" : \"access-rule\",\n      \"domain\" : {\n        \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n        \"name\" : \"SMC User\",\n        \"domain-type\" : \"domain\"\n      },\n      \"icon\" : \"Objects/accessRule\",\n      \"color\" : \"black\",\n      \"rule-number\" : 2\n    }, {\n      \"uid\" : \"694b37a1-24eb-4a08-933f-a461f3f548e7\",\n      \"name\" : \"rule 3\",\n      \"type\" : \"access-rule\",\n      \"domain\" : {\n        \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n        \"name\" : \"SMC User\",\n        \"domain-type\" : \"domain\"\n      },\n      \"icon\" : \"Objects/accessRule\",\n      \"color\" : \"black\",\n      \"rule-number\" : 3\n    }, {\n      \"uid\" : \"e5957034-ad33-483e-baca-246177077dac\",\n      \"name\" : \"section\",\n      \"type\" : \"access-section\",\n      \"domain\" : {\n        \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n        \"name\" : \"SMC User\",\n        \"domain-type\" : \"domain\"\n      },\n      \"tags\" : [ ],\n      \"read-only\" : false,\n      \"comments\" : \"\",\n      \"color\" : \"black\",\n      \"icon\" : \"General/globalsNa\",\n      \"from-rule\" : 4,\n      \"to-rule\" : 5,\n      \"children\" : [ {\n        \"uid\" : \"23bad176-b95e-4eff-9d28-9ef3c3295c6f\",\n        \"name\" : \"rule 4\",\n        \"type\" : \"access-rule\",\n        \"domain\" : {\n          \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n          \"name\" : \"SMC User\",\n          \"domain-type\" : \"domain\"\n        },\n        \"icon\" : \"Objects/accessRule\",\n        \"color\" : \"black\",\n        \"rule-number\" : 4\n      }, {\n        \"uid\" : \"1a839873-754b-4d7f-95fa-e41c2a6d5d52\",\n        \"name\" : \"Cleanup rule\",\n        \"type\" : \"access-rule\",\n        \"domain\" : {\n          \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n          \"name\" : \"SMC User\",\n          \"domain-type\" : \"domain\"\n        },\n        \"icon\" : \"Objects/accessRule\",\n        \"color\" : \"black\",\n        \"rule-number\" : 5\n      } ]\n    } ]\n  }\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:25.699796",
    "source_file": "show-layer-structure.html"
  }
}
```