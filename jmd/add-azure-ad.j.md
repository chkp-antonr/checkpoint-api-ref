# add-azure-ad

```json
{
  "command": "add-azure-ad",
  "description": "Create a new Microsoft Entra ID object (formerly, Azure AD). Microsoft Entra ID is Microsoft's cloud-based identity and access management service.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/add-azure-ad",
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
        "name": "authentication-method",
        "description": "user-authenticationUses the Azure AD User to authenticate.service-principal-authenticationUses the Service Principal to authenticate.",
        "type": "string",
        "required": true,
        "valid_values": [
          "user-authentication",
          "service-principal-authentication"
        ]
      },
      {
        "name": "password",
        "description": "Password of the Azure account.Required for authentication-method:user-authentication.",
        "type": "string",
        "required": true
      },
      {
        "name": "username",
        "description": "An Azure Active Directory user Format<username>@<domain>.Required for authentication-method:user-authentication.",
        "type": "string",
        "required": true
      },
      {
        "name": "application-id",
        "description": "The Application ID of the Service Principal, in UUID format.Required for authentication-method:service-principal-authentication.",
        "type": "string",
        "required": true
      },
      {
        "name": "application-key",
        "description": "The key created for the Service Principal.Required for authentication-method:service-principal-authentication.",
        "type": "string",
        "required": true
      },
      {
        "name": "directory-id",
        "description": "The Directory ID of the Azure AD, in UUID format.Required for authentication-method:service-principal-authentication.",
        "type": "string",
        "required": true
      }
    ]
  },
  "response": {
    "success": [
      {
        "name": "task-id",
        "description": "Azure AD Operation task-id, use show-task command to check the progress of the task.",
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
    "add-azure-ad-object": {
      "description": "Add Microsoft Azure Active Directory.Use the show-task command to check the progress of the task. Output below is the output of the show-task command.",
      "request": "POST {{server}}/add-azure-ad\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"my_azureAD\",\n  \"authentication-method\" : \"service-principal-authentication\",\n  \"application-id\" : \"a8662b33-306f-42ba-9ffb-a0ac27c8903f\",\n  \"application-key\" : \"EjdJ2JcNGpw3[GV8:PMN_s2KH]JhtlpO\",\n  \"directory-id\" : \"19c063a8-3bee-4ea5-b984-e344asds37f7\"\n}",
      "response": "{\n  \"tasks\" : [ {\n    \"task-name\" : \"Data Center Operation\",\n    \"task-id\" : \"01234567-89ab-cdef-b4ab-a5aefde29b2e\",\n    \"status\" : \"succeeded\",\n    \"progress-percentage\" : 100,\n    \"suppressed\" : false,\n    \"task-details\" : [ ]\n  } ]\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:06.589898",
    "source_file": "add-azure-ad.html"
  }
}
```