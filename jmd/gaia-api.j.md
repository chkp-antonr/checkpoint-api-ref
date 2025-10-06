# gaia-api

```json
{
  "command": "gaia-api",
  "description": "Runs a gaia-api command from the management. Syntax: gaia-api/gateway-command. Gateway-command is the gaia-api command which you want to send the request. Please take a look at the examples to know how to use it. Please include any input parameters needed in the request body. The cache config file in $FWDIR/api/conf/cache.conf can be used to change the settings. NOTE: Please add a rule to allow the connection from the management to the targets.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/gaia-api",
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
        "name": "target",
        "description": "Gateway-object-name or gateway-ip-address or gateway-UID.",
        "type": "string",
        "required": true
      },
      {
        "name": "other-parameter",
        "description": "Other input parameters that gateway needs it.",
        "type": "string",
        "required": false
      }
    ]
  },
  "response": {
    "success": [
      {
        "name": "command-name",
        "description": "Target's api command.",
        "type": "string",
        "required": false
      },
      {
        "name": "response-message",
        "description": "Response's object from the target in json format.",
        "type": "Object",
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
    "show-asset (gaia-api with gateway UID)": {
      "description": "",
      "request": "POST {{server}}/gaia-api/show-asset\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"target\" : \"52048978-c507-8243-9d84-074d11154616\"\n}",
      "response": "{\n  \"command-name\" : \"show-asset\",\n  \"response-message\" : {\n    \"ac\" : [ ],\n    \"disk\" : [ ],\n    \"lom-info\" : [ ],\n    \"memory\" : [ ],\n    \"network\" : [ ],\n    \"power-supply\" : [ ],\n    \"sam\" : [ ],\n    \"system\" : [ {\n      \"key\" : \"Platform\",\n      \"value\" : \"VMware Virtual Platform\"\n    }, {\n      \"key\" : \"CPU Model\",\n      \"value\" : \"Intel(R) Xeon(R) CPU E5-2630 v2\"\n    }, {\n      \"key\" : \"CPU Frequency\",\n      \"value\" : \"2593.500 Mhz\"\n    }, {\n      \"key\" : \"Number of Cores\",\n      \"value\" : \"4\"\n    }, {\n      \"key\" : \"CPU Hyperthreading\",\n      \"value\" : \"Disabled\"\n    } ]\n  }\n}"
    },
    "show-diagnostics (gaia-api with input parameters and version)": {
      "description": "",
      "request": "POST {{server}}/gaia-api/v1.3/show-diagnostics\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"target\" : \"192.168.1.1\",\n  \"category\" : \"os\",\n  \"topic\" : \"disk\"\n}",
      "response": "{\n  \"command-name\" : \"v1.3/show-diagnostics\",\n  \"response-message\" : {\n    \"from\" : 1,\n    \"objects\" : [ {\n      \"free\" : 28636692480,\n      \"partition\" : \"/\",\n      \"total\" : 34342961152,\n      \"used\" : 5706268672\n    }, {\n      \"free\" : 261779456,\n      \"partition\" : \"/boot\",\n      \"total\" : 304624640,\n      \"used\" : 42845184\n    }, {\n      \"free\" : 34069254144,\n      \"partition\" : \"/var/log\",\n      \"total\" : 34342961152,\n      \"used\" : 273707008\n    } ],\n    \"to\" : 3,\n    \"total\" : 3\n  }\n}"
    },
    "show-hostname (gaia-api without input parameter)": {
      "description": "",
      "request": "POST {{server}}/gaia-api/show-hostname\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"target\" : \"192.168.1.1\"\n}",
      "response": "{\n  \"command-name\" : \"show-hostname\",\n  \"response-message\" : {\n    \"name\" : \"gw-832546\"\n  }\n}"
    },
    "show-interface (gaia-api with input parameter)": {
      "description": "",
      "request": "POST {{server}}/gaia-api/show-interface\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"target\" : \"192.168.1.1\",\n  \"name\" : \"eth0\"\n}",
      "response": "{\n  \"command-name\" : \"show-interface\",\n  \"response-message\" : {\n    \"comments\" : \"\",\n    \"enabled\" : true,\n    \"ipv4-address\" : \"192.168.1.1\",\n    \"ipv4-mask-length\" : \"24\",\n    \"ipv6-address\" : \"Not-Configured\",\n    \"ipv6-autoconfig\" : \"Not configured\",\n    \"ipv6-local-link-address\" : \"Not Configured\",\n    \"ipv6-mask-length\" : \"Not-Configured\",\n    \"name\" : \"eth0\",\n    \"type\" : \"physical\"\n  }\n}"
    },
    "show-version (gaia-api with object name)": {
      "description": "",
      "request": "POST {{server}}/gaia-api/v1.2/show-version\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"target\" : \"gw-123456\"\n}",
      "response": "{\n  \"command-name\" : \"v1.2/show-version\",\n  \"response-message\" : {\n    \"os-build\" : \"111\",\n    \"os-edition\" : \"64-bit\",\n    \"os-kernel-version\" : \"3.10.0-693cpx86_64\",\n    \"product-version\" : \"Check Point Gaia R80.30\"\n  }\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:15.398632",
    "source_file": "gaia-api.html"
  }
}
```