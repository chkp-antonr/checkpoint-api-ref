# show-data-types-patterns

```json
{
  "command": "show-data-types-patterns",
  "description": "Retrieve all Pattern Data Type objects.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/show-data-types-patterns",
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
    "show-data-types-patterns": {
      "description": "",
      "request": "POST {{server}}/show-data-types-patterns\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{ }",
      "response": "{\n  \"from\" : 1,\n  \"to\" : 15,\n  \"total\" : 15,\n  \"objects\" : [ {\n    \"uid\" : \"1a4eccb6-31d6-458d-aa80-f73e038e241b\",\n    \"name\" : \"ABA Transit Numbers\",\n    \"type\" : \"data-type-patterns\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"icon\" : \"DataLossPrevention/Data_Object\",\n    \"color\" : \"forest green\"\n  }, {\n    \"uid\" : \"eaae644f-e2fc-4401-829a-a7195a2b0fe3\",\n    \"name\" : \"CUSIP Number\",\n    \"type\" : \"data-type-patterns\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"icon\" : \"DataLossPrevention/Data_Object\",\n    \"color\" : \"forest green\"\n  }, {\n    \"uid\" : \"e4c7b48b-4dfe-427a-853e-1a4226249950\",\n    \"name\" : \"HIPAA - Medical Record Number - MRN\",\n    \"type\" : \"data-type-patterns\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"icon\" : \"DataLossPrevention/Data_Object\",\n    \"color\" : \"dark blue\"\n  }, {\n    \"uid\" : \"8f057ffc-6a2e-492e-b0ab-596877ecf7bb\",\n    \"name\" : \"International Bank Account Number - IBAN\",\n    \"type\" : \"data-type-patterns\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"icon\" : \"DataLossPrevention/Data_Object\",\n    \"color\" : \"forest green\"\n  }, {\n    \"uid\" : \"e4e524d3-4888-4575-a15a-9a452daf1723\",\n    \"name\" : \"International Securities Identification Number - ISIN\",\n    \"type\" : \"data-type-patterns\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"icon\" : \"DataLossPrevention/Data_Object\",\n    \"color\" : \"forest green\"\n  }, {\n    \"uid\" : \"af92af6c-3a9c-4c2f-9040-c11c1b5770a8\",\n    \"name\" : \"IPI - Details of Payment Code\",\n    \"type\" : \"data-type-patterns\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"icon\" : \"DataLossPrevention/Data_Object\",\n    \"color\" : \"forest green\"\n  }, {\n    \"uid\" : \"3ce61848-a025-4385-b92d-8d9773099302\",\n    \"name\" : \"MAC Address\",\n    \"type\" : \"data-type-patterns\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"icon\" : \"DataLossPrevention/Data_Object\",\n    \"color\" : \"navy blue\"\n  }, {\n    \"uid\" : \"11809b0f-a42f-438a-9886-1f532ebf41b4\",\n    \"name\" : \"Machine Readable Passport Numbers\",\n    \"type\" : \"data-type-patterns\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"icon\" : \"DataLossPrevention/Data_Object\",\n    \"color\" : \"red\"\n  }, {\n    \"uid\" : \"7d6e8f77-0f08-49c4-b5d0-4bcf4af9fec7\",\n    \"name\" : \"pattern-obj\",\n    \"type\" : \"data-type-patterns\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"icon\" : \"DataLossPrevention/Data_Object\",\n    \"color\" : \"black\"\n  }, {\n    \"uid\" : \"16581df4-2c94-45d0-8203-0e8a72b43523\",\n    \"name\" : \"PCI - Credit Card Numbers\",\n    \"type\" : \"data-type-patterns\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"icon\" : \"DataLossPrevention/Data_Object\",\n    \"color\" : \"dark blue\"\n  }, {\n    \"uid\" : \"803a2243-961f-43f6-a527-ad1e5f5ca458\",\n    \"name\" : \"Personal Information Exchange File\",\n    \"type\" : \"data-type-patterns\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"icon\" : \"DataLossPrevention/Data_Object\",\n    \"color\" : \"navy blue\"\n  }, {\n    \"uid\" : \"5fc6b546-1ff7-460e-8dc0-608bdbfb7c66\",\n    \"name\" : \"SEDOL Codes\",\n    \"type\" : \"data-type-patterns\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"icon\" : \"DataLossPrevention/Data_Object\",\n    \"color\" : \"forest green\"\n  }, {\n    \"uid\" : \"4c55cff2-fd7b-4262-9e6d-a6f0ffe41245\",\n    \"name\" : \"SIM Serial Number - ICC-ID\",\n    \"type\" : \"data-type-patterns\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"icon\" : \"DataLossPrevention/Data_Object\",\n    \"color\" : \"red\"\n  }, {\n    \"uid\" : \"3d44e948-50ce-43a6-bd6c-bbdaa6775e26\",\n    \"name\" : \"U.S. Social Security Numbers - According to SSA\",\n    \"type\" : \"data-type-patterns\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"icon\" : \"DataLossPrevention/Data_Object\",\n    \"color\" : \"red\"\n  }, {\n    \"uid\" : \"87e7c6ab-729b-419d-bff0-7bdd06280c7a\",\n    \"name\" : \"Vehicle Identification Number - VIN\",\n    \"type\" : \"data-type-patterns\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"icon\" : \"DataLossPrevention/Data_Object\",\n    \"color\" : \"forest green\"\n  } ]\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:23.996681",
    "source_file": "show-data-types-patterns.html"
  }
}
```