# show-tags

```json
{
  "command": "show-tags",
  "description": "Retrieve all objects.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/show-tags",
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
    "show-tags": {
      "description": "Show all the tags",
      "request": "POST {{server}}/show-tags\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{ }",
      "response": "{\n  \"from\" : 1,\n  \"to\" : 15,\n  \"total\" : 15,\n  \"objects\" : [ {\n    \"folder\" : {\n      \"uid\" : \"a7a569db-cd04-4f1c-bc8d-94dbfc22b150\",\n      \"name\" : \"Check Point Settings\"\n    },\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    },\n    \"type\" : \"tag\",\n    \"name\" : \"DMZ related\",\n    \"uid\" : \"bcbace1f-aead-44da-9bff-56bdb1e4c4d2\"\n  }, {\n    \"folder\" : {\n      \"uid\" : \"a7a569db-cd04-4f1c-bc8d-94dbfc22b150\",\n      \"name\" : \"Check Point Settings\"\n    },\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    },\n    \"type\" : \"tag\",\n    \"name\" : \"England\",\n    \"uid\" : \"50877af4-4a17-4ff0-8f77-de0784e8f1ab\"\n  }, {\n    \"folder\" : {\n      \"uid\" : \"a7a569db-cd04-4f1c-bc8d-94dbfc22b150\",\n      \"name\" : \"Check Point Settings\"\n    },\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    },\n    \"type\" : \"tag\",\n    \"name\" : \"Europe\",\n    \"uid\" : \"89e6ee92-d01b-48e2-98a3-626e644d6ff9\"\n  }, {\n    \"folder\" : {\n      \"uid\" : \"a7a569db-cd04-4f1c-bc8d-94dbfc22b150\",\n      \"name\" : \"Check Point Settings\"\n    },\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    },\n    \"type\" : \"tag\",\n    \"name\" : \"France\",\n    \"uid\" : \"de21ae82-f7d6-4a3b-b49c-dc53a51def1d\"\n  }, {\n    \"folder\" : {\n      \"uid\" : \"a7a569db-cd04-4f1c-bc8d-94dbfc22b150\",\n      \"name\" : \"Check Point Settings\"\n    },\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    },\n    \"type\" : \"tag\",\n    \"name\" : \"Important assets\",\n    \"uid\" : \"c9ddb2b2-40a6-422a-a6ea-6c3214f8cf4b\"\n  }, {\n    \"folder\" : {\n      \"uid\" : \"a7a569db-cd04-4f1c-bc8d-94dbfc22b150\",\n      \"name\" : \"Check Point Settings\"\n    },\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    },\n    \"type\" : \"tag\",\n    \"name\" : \"London\",\n    \"uid\" : \"5a7a1f46-10b1-461d-b8c0-596c380dd05d\"\n  }, {\n    \"folder\" : {\n      \"uid\" : \"a25a7783-9adb-4a65-9850-b97ee7860530\",\n      \"name\" : \"/Global Objects\"\n    },\n    \"domain\" : {\n      \"domain-type\" : \"local domain\",\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\"\n    },\n    \"type\" : \"tag\",\n    \"name\" : \"My New Tag\",\n    \"uid\" : \"4995cbc3-ce01-4b2e-b6ac-bb48baee89e3\"\n  }, {\n    \"folder\" : {\n      \"uid\" : \"a25a7783-9adb-4a65-9850-b97ee7860530\",\n      \"name\" : \"/Global Objects\"\n    },\n    \"domain\" : {\n      \"domain-type\" : \"local domain\",\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\"\n    },\n    \"type\" : \"tag\",\n    \"name\" : \"My New Tag21\",\n    \"uid\" : \"728a4212-a521-46a2-a5a1-b6536a9aecd5\"\n  }, {\n    \"folder\" : {\n      \"uid\" : \"a7a569db-cd04-4f1c-bc8d-94dbfc22b150\",\n      \"name\" : \"Check Point Settings\"\n    },\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    },\n    \"type\" : \"tag\",\n    \"name\" : \"New York\",\n    \"uid\" : \"771878c4-990f-47b9-9249-1838163014e6\"\n  }, {\n    \"folder\" : {\n      \"uid\" : \"a7a569db-cd04-4f1c-bc8d-94dbfc22b150\",\n      \"name\" : \"Check Point Settings\"\n    },\n    \"domain\" : {\n      \"domain-type\" : \"data domain\",\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\"\n    },\n    \"type\" : \"tag\",\n    \"name\" : \"Paris\",\n    \"uid\" : \"16058757-98a1-4ed6-9926-c5fbfa192c52\"\n  }, {\n    \"folder\" : {\n      \"uid\" : \"a25a7783-9adb-4a65-9850-b97ee7860530\",\n      \"name\" : \"/Global Objects\"\n    },\n    \"domain\" : {\n      \"domain-type\" : \"local domain\",\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\"\n    },\n    \"type\" : \"tag\",\n    \"name\" : \"my tag\",\n    \"uid\" : \"f96b37ec-e22e-4945-8bbf-d37b117914e0\"\n  }, {\n    \"folder\" : {\n      \"uid\" : \"a25a7783-9adb-4a65-9850-b97ee7860530\",\n      \"name\" : \"/Global Objects\"\n    },\n    \"domain\" : {\n      \"domain-type\" : \"local domain\",\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\"\n    },\n    \"type\" : \"tag\",\n    \"name\" : \"my tag1\",\n    \"uid\" : \"9f51e2b6-696a-4f28-9239-5b0622fce1e5\"\n  }, {\n    \"folder\" : {\n      \"uid\" : \"a25a7783-9adb-4a65-9850-b97ee7860530\",\n      \"name\" : \"/Global Objects\"\n    },\n    \"domain\" : {\n      \"domain-type\" : \"local domain\",\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\"\n    },\n    \"type\" : \"tag\",\n    \"name\" : \"tag1\",\n    \"uid\" : \"687715ca-674b-4642-981b-b6243fde04c0\"\n  }, {\n    \"folder\" : {\n      \"uid\" : \"a25a7783-9adb-4a65-9850-b97ee7860530\",\n      \"name\" : \"/Global Objects\"\n    },\n    \"domain\" : {\n      \"domain-type\" : \"local domain\",\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\"\n    },\n    \"type\" : \"tag\",\n    \"name\" : \"tag2\",\n    \"uid\" : \"f1ee4a33-6577-45da-9d4f-cc352a349c80\"\n  }, {\n    \"folder\" : {\n      \"uid\" : \"a25a7783-9adb-4a65-9850-b97ee7860530\",\n      \"name\" : \"/Global Objects\"\n    },\n    \"domain\" : {\n      \"domain-type\" : \"local domain\",\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\"\n    },\n    \"type\" : \"tag\",\n    \"name\" : \"tag3\",\n    \"uid\" : \"dda885bb-0d5b-4529-96eb-55b757847092\"\n  } ]\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:28.656852",
    "source_file": "show-tags.html"
  }
}
```