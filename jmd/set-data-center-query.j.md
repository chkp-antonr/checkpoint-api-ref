# set-data-center-query

```json
{
  "command": "set-data-center-query",
  "description": "Edit existing data center query.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/set-data-center-query",
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
        "name": "data-centers",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "add",
        "description": "Adds to collection of values",
        "type": "string",
        "required": false
      },
      {
        "name": "remove",
        "description": "Removes from collection of values",
        "type": "string",
        "required": false
      },
      {
        "name": "new-name",
        "description": "New name of the object.",
        "type": "string",
        "required": false
      },
      {
        "name": "query-rules",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "predefined",
          "tag"
        ]
      },
      {
        "name": "key-type",
        "description": "The type of the \"key\" parameter.Use \"predefined\" for these keys: type-in-data-center, name-in-data-center, and ip-address.Use \"tag\" to query the Data Center tag's property.",
        "type": "string",
        "required": true,
        "valid_values": [
          "predefined",
          "tag"
        ]
      },
      {
        "name": "key",
        "description": "Defines in which Data Center property to query.For key-type \"predefined\", use these keys: type-in-data-center, name-in-data-center, and ip-address.For key-type \"tag\", use the Data Center tag key to query.Keys are case-insensitive.",
        "type": "string",
        "required": true
      },
      {
        "name": "values",
        "description": "The value(s) of the Data Center property to match the Query Rule.Values are case-insensitive.There is an 'OR' operation between multiple values.For key-type \"predefined\" and key 'ip-address', the values must be an IPv4 or IPv6 address.For key-type \"tag\", the values must be the Data Center tag values.",
        "type": "array",
        "required": false
      },
      {
        "name": "key-type",
        "description": "The type of the \"key\" parameter.Use \"predefined\" for these keys: type-in-data-center, name-in-data-center, and ip-address.Use \"tag\" to query the Data Center tag's property.",
        "type": "string",
        "required": true,
        "valid_values": [
          "predefined",
          "tag"
        ]
      },
      {
        "name": "key",
        "description": "Defines in which Data Center property to query.For key-type \"predefined\", use these keys: type-in-data-center, name-in-data-center, and ip-address.For key-type \"tag\", use the Data Center tag key to query.Keys are case-insensitive.",
        "type": "string",
        "required": true
      },
      {
        "name": "values",
        "description": "The value(s) of the Data Center property to match the Query Rule.Values are case-insensitive.There is an 'OR' operation between multiple values.For key-type \"predefined\" and key 'ip-address', the values must be an IPv4 or IPv6 address.For key-type \"tag\", the values must be the Data Center tag values.",
        "type": "array",
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
        "name": "data-centers",
        "description": "Data Center Servers.",
        "type": "array",
        "required": false
      },
      {
        "name": "query-rules",
        "description": "Data Center Query Rules.",
        "type": "array",
        "required": false
      },
      {
        "name": "using-all-data-center",
        "description": "Using all Data Centers.",
        "type": "boolean",
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
    "set-data-center-query add Data Center Server": {
      "description": "Add a Data Center Server to an existing Data Center Query",
      "request": "POST {{server}}/set-data-center-query\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"data-centers\" : {\n    \"add\" : [ \"data-center2\" ]\n  },\n  \"name\" : \"data-center-query1\"\n}",
      "response": "{\n  \"uid\" : \"8024422d-74c2-487e-a196-a8649e3f88da\",\n  \"name\" : \"data-center-query1\",\n  \"type\" : \"data-center-query\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1591515377210,\n      \"iso-8601\" : \"2020-06-07T10:36+0300\"\n    },\n    \"last-modifier\" : \"WEB_API\",\n    \"creation-time\" : {\n      \"posix\" : 1591513615720,\n      \"iso-8601\" : \"2020-06-07T10:06+0300\"\n    },\n    \"creator\" : \"WEB_API\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : true,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"NetworkObjects/ExternalDataSource\",\n  \"query-rules\" : [ {\n    \"uid\" : \"20387286-f498-4620-a5fb-7de596ba721c\",\n    \"type\" : \"DataCenterQueryRule\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"meta-info\" : {\n      \"lock\" : \"unlocked\",\n      \"validation-state\" : \"ok\"\n    },\n    \"tags\" : [ ],\n    \"read-only\" : true,\n    \"comments\" : \"\",\n    \"color\" : \"black\",\n    \"icon\" : \"NetworkObjects/ExternalDataSource\",\n    \"key-type\" : \"PREDEFINED\",\n    \"key\" : \"name-in-data-center\",\n    \"values\" : [ \"myvalue\" ]\n  } ],\n  \"data-centers\" : [ {\n    \"uid\" : \"088d2439-5c0c-4223-a9ca-afc7da9df4d2\",\n    \"name\" : \"data-center1\",\n    \"type\" : \"data-center-server\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    }\n  }, {\n    \"uid\" : \"7a6f32d9-8667-45e7-ac90-b858df32d76c\",\n    \"name\" : \"data-center2\",\n    \"type\" : \"data-center-server\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    }\n  } ],\n  \"using-all-data-center\" : false\n}"
    },
    "set-data-center-query remove Data Center Server": {
      "description": "Remove a Data Center Server from an existing Data Center Query",
      "request": "POST {{server}}/set-data-center-query\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"data-centers\" : {\n    \"remove\" : [ \"data-center2\" ]\n  },\n  \"name\" : \"data-center-query1\"\n}",
      "response": "{\n  \"uid\" : \"8024422d-74c2-487e-a196-a8649e3f88da\",\n  \"name\" : \"data-center-query1\",\n  \"type\" : \"data-center-query\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1591519199187,\n      \"iso-8601\" : \"2020-06-07T11:39+0300\"\n    },\n    \"last-modifier\" : \"WEB_API\",\n    \"creation-time\" : {\n      \"posix\" : 1591513615720,\n      \"iso-8601\" : \"2020-06-07T10:06+0300\"\n    },\n    \"creator\" : \"WEB_API\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : true,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"NetworkObjects/ExternalDataSource\",\n  \"query-rules\" : [ {\n    \"uid\" : \"20387286-f498-4620-a5fb-7de596ba721c\",\n    \"type\" : \"DataCenterQueryRule\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"meta-info\" : {\n      \"lock\" : \"unlocked\",\n      \"validation-state\" : \"ok\"\n    },\n    \"tags\" : [ ],\n    \"read-only\" : true,\n    \"comments\" : \"\",\n    \"color\" : \"black\",\n    \"icon\" : \"NetworkObjects/ExternalDataSource\",\n    \"key-type\" : \"PREDEFINED\",\n    \"key\" : \"name-in-data-center\",\n    \"values\" : [ \"myvalue\" ]\n  } ],\n  \"data-centers\" : [ {\n    \"uid\" : \"088d2439-5c0c-4223-a9ca-afc7da9df4d2\",\n    \"name\" : \"data-center1\",\n    \"type\" : \"data-center-server\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    }\n  } ],\n  \"using-all-data-center\" : false\n}"
    },
    "set-data-center-query set Data Center Servers to All": {
      "description": "Set All Data Centers for a Data Center Query",
      "request": "POST {{server}}/set-data-center-query\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"data-centers\" : {\n    \"set\" : \"All\"\n  },\n  \"name\" : \"data-center-query1\"\n}",
      "response": "{\n  \"uid\" : \"8024422d-74c2-487e-a196-a8649e3f88da\",\n  \"name\" : \"data-center-query1\",\n  \"type\" : \"data-center-query\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1591519435090,\n      \"iso-8601\" : \"2020-06-07T11:43+0300\"\n    },\n    \"last-modifier\" : \"WEB_API\",\n    \"creation-time\" : {\n      \"posix\" : 1591513615720,\n      \"iso-8601\" : \"2020-06-07T10:06+0300\"\n    },\n    \"creator\" : \"WEB_API\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : true,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"NetworkObjects/ExternalDataSource\",\n  \"query-rules\" : [ {\n    \"uid\" : \"20387286-f498-4620-a5fb-7de596ba721c\",\n    \"type\" : \"DataCenterQueryRule\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"meta-info\" : {\n      \"lock\" : \"unlocked\",\n      \"validation-state\" : \"ok\"\n    },\n    \"tags\" : [ ],\n    \"read-only\" : true,\n    \"comments\" : \"\",\n    \"color\" : \"black\",\n    \"icon\" : \"NetworkObjects/ExternalDataSource\",\n    \"key-type\" : \"PREDEFINED\",\n    \"key\" : \"name-in-data-center\",\n    \"values\" : [ \"myvalue\" ]\n  } ],\n  \"data-centers\" : [ ],\n  \"using-all-data-center\" : true\n}"
    },
    "set-data-center-query set query rules": {
      "description": "Set new query rules",
      "request": "POST {{server}}/set-data-center-query\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"data-center-query1\",\n  \"query-rules\" : {\n    \"key\" : \"name-in-data-center\",\n    \"key-type\" : \"predefined\",\n    \"values\" : [ \"myName2\" ]\n  }\n}",
      "response": "{\n  \"uid\" : \"27462eb6-f386-48b3-8986-12aaa56b587d\",\n  \"name\" : \"data-center-query1\",\n  \"type\" : \"data-center-query\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1594640753251,\n      \"iso-8601\" : \"2020-07-13T14:45+0300\"\n    },\n    \"last-modifier\" : \"WEB_API\",\n    \"creation-time\" : {\n      \"posix\" : 1594640634151,\n      \"iso-8601\" : \"2020-07-13T14:43+0300\"\n    },\n    \"creator\" : \"aa\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : true,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"NetworkObjects/ExternalDataQuery\",\n  \"query-rules\" : [ {\n    \"uid\" : \"832c3f41-7e2d-4223-9357-6e661c32dea1\",\n    \"type\" : \"DataCenterQueryRule\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"meta-info\" : {\n      \"lock\" : \"unlocked\",\n      \"validation-state\" : \"ok\"\n    },\n    \"tags\" : [ ],\n    \"read-only\" : true,\n    \"comments\" : \"\",\n    \"color\" : \"black\",\n    \"icon\" : \"NetworkObjects/ExternalDataQuery\",\n    \"key-type\" : \"PREDEFINED\",\n    \"key\" : \"Name in Data Center\",\n    \"values\" : [ \"myName2\" ]\n  } ],\n  \"data-centers\" : [ ],\n  \"using-all-data-center\" : true\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:16.367827",
    "source_file": "set-data-center-query.html"
  }
}
```