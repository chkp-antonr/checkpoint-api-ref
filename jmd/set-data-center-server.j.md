# set-data-center-server

```json
{
  "command": "set-data-center-server",
  "description": "Edit existing Data Center Server using name or uid. Data Center Server represents the connection to a cloud environment. The Data Center Server contains Data Center Objects, these objects can be imported from it using the add-data-center-object command.Note: Each Data Center Server type uses additional dedicated arguments, see arguments per Data Center Server type.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/set-data-center-server",
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
        "name": "new-name",
        "description": "New name of the object.",
        "type": "string",
        "required": false
      }
    ]
  },
  "response": {
    "success": [
      {
        "name": "task-id",
        "description": "Data Center Operation task-id, use show-task command to check the progress of the task.",
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
    "set-data-center-server type AWS": {
      "description": "Set any argument for a data center server of type AWS,Use the show-task command to check the progress of the task. Output below is the output of the show-task command.",
      "request": "POST {{server}}/set-data-center-server\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"my_aws\",\n  \"access-key-id\" : \"AWS_ACCESS_KEY\",\n  \"secret-access-key\" : \"AWS_SECRET_KEY\"\n}",
      "response": "{\n  \"tasks\" : [ {\n    \"task-name\" : \"Data Center Operation\",\n    \"task-id\" : \"01234567-89ab-cdef-b4ab-a5aefde29b2e\",\n    \"status\" : \"succeeded\",\n    \"progress-percentage\" : 100,\n    \"suppressed\" : false,\n    \"task-details\" : [ ]\n  } ]\n}"
    },
    "set-data-center-server type Cisco ACI": {
      "description": "Set any argument for a data center server of type Cisco ACI,Use the show-task command to check the progress of the task. Output below is the output of the show-task command.",
      "request": "POST {{server}}/set-data-center-server\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"my_aci\",\n  \"urls\" : [ \"https://1.1.1.1\", \"https://2.2.2.2\" ],\n  \"username\" : \"admin\"\n}",
      "response": "{\n  \"tasks\" : [ {\n    \"task-name\" : \"Data Center Operation\",\n    \"task-id\" : \"01234567-89ab-cdef-b4ab-a5aefde29b2e\",\n    \"status\" : \"succeeded\",\n    \"progress-percentage\" : 100,\n    \"suppressed\" : false,\n    \"task-details\" : [ ]\n  } ]\n}"
    },
    "set-data-center-server type Cisco ISE": {
      "description": "Set any argument for a data center server of type Cisco ISE,Use the show-task command to check the progress of the task. Output below is the output of the show-task command.",
      "request": "POST {{server}}/set-data-center-server\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"my_ise\",\n  \"new-name\" : \"ise_new_admin\",\n  \"color\" : \"red\",\n  \"username\" : \"newAdmin\",\n  \"password-base64\" : \"YWRtaW4=\"\n}",
      "response": "{\n  \"tasks\" : [ {\n    \"task-name\" : \"Data Center Operation\",\n    \"task-id\" : \"01234567-89ab-cdef-b4ab-a5aefde29b2e\",\n    \"status\" : \"succeeded\",\n    \"progress-percentage\" : 100,\n    \"suppressed\" : false,\n    \"task-details\" : [ ]\n  } ]\n}"
    },
    "set-data-center-server type Google Cloud Platform": {
      "description": "Set the authentication method of a data center server of type Google Cloud Platform.Make sure to provide all the required arguments for the new authentication method,Use the show-task command to check the progress of the task. Output below is the output of the show-task command.",
      "request": "POST {{server}}/set-data-center-server\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"my_gcp\",\n  \"authentication-method\" : \"key-authentication\",\n  \"private-key\" : \"wzVi9CcnFIT09JOFV1c0ZQRW9OQmtKU1k4UGxjeWlOXG5TZ1loV3FhZ2tITkl1RmE5MnhkMXJQMy9ZajFKWjVYeUdmM0FYZ3ZndFFLQmdRQyszNkVPQVdua01YZlByR0pQXG5rcmtEelJHNERnVTNNTDcwRkpCZldYbXBNaVAzQm53ZHljTkU0L0E4Zjh1RWpVOE0zU3FZWEtGbURIUDFwR1RxXG5yTzFFNnQzaVVTR2IrQkpMZjV6MGMweEM1SjVWM0VUYlNVT25sNXVOZXNhZUFWd0hDZncvY2Y1WDRjUlZQU1V0XG50S1Q3Q2Q1MXRBUUxFdm5TUC9FVXhZL0Qyd0tCZ1FDMWlSa1FqcndwUmVLUFlwRkJWSnAQ09nckhBbXdRa2hFa096clVtS3BOZURrRFlEMVV6cjY3Nk9ZXG5DdmR2YWRhdGEveDUwOS9ndXloaWwlNDBjaGtwLWRldi5pYW0uZ3NlcnZpY2VhY2NvdW50LmNvbSIKfQo=\"\n}",
      "response": "{\n  \"tasks\" : [ {\n    \"task-name\" : \"Data Center Operation\",\n    \"task-id\" : \"01234567-89ab-cdef-b4ab-a5aefde29b2e\",\n    \"status\" : \"succeeded\",\n    \"progress-percentage\" : 100,\n    \"suppressed\" : false,\n    \"task-details\" : [ ]\n  } ]\n}"
    },
    "set-data-center-server type Generic Data Center": {
      "description": "Set any argument for a data center server of type Generic Data Center,Use the show-task command to check the progress of the task. Output below is the output of the show-task command.",
      "request": "POST {{server}}/set-data-center-server\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"my_genericDC\",\n  \"interval\" : \"20\"\n}",
      "response": "{\n  \"tasks\" : [ {\n    \"task-name\" : \"Data Center Operation\",\n    \"task-id\" : \"01234567-89ab-cdef-b4ab-a5aefde29b2e\",\n    \"status\" : \"succeeded\",\n    \"progress-percentage\" : 100,\n    \"suppressed\" : false,\n    \"task-details\" : [ ]\n  } ]\n}"
    },
    "set-data-center-server type Microsoft Azure": {
      "description": "Set the authentication method of a data center server of type Microsoft Azure.Make sure to provide all the required arguments for the new authentication method,Use the show-task command to check the progress of the task. Output below is the output of the show-task command.",
      "request": "POST {{server}}/set-data-center-server\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"my_azure\",\n  \"authentication-method\" : \"user-authentication\",\n  \"username\" : \"username@company.onmicrosoft.com\",\n  \"password-base64\" : \"YWRtaW4=\"\n}",
      "response": "{\n  \"tasks\" : [ {\n    \"task-name\" : \"Data Center Operation\",\n    \"task-id\" : \"01234567-89ab-cdef-b4ab-a5aefde29b2e\",\n    \"status\" : \"succeeded\",\n    \"progress-percentage\" : 100,\n    \"suppressed\" : false,\n    \"task-details\" : [ ]\n  } ]\n}"
    },
    "set-data-center-server type Nuage": {
      "description": "Trust a new certificate for a data center server of type Nuage,Use the show-task command to check the progress of the task. Output below is the output of the show-task command.",
      "request": "POST {{server}}/set-data-center-server\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"my_nuage\",\n  \"certificate-fingerprint\" : \"2a0a14743a235a440a7cba263a3d8ab44324dad4\"\n}",
      "response": "{\n  \"tasks\" : [ {\n    \"task-name\" : \"Data Center Operation\",\n    \"task-id\" : \"01234567-89ab-cdef-b4ab-a5aefde29b2e\",\n    \"status\" : \"succeeded\",\n    \"progress-percentage\" : 100,\n    \"suppressed\" : false,\n    \"task-details\" : [ ]\n  } ]\n}"
    },
    "set-data-center-server type Nutanix": {
      "description": "Set any argument for a data center server of type Nutanix,Use the show-task command to check the progress of the task. Output below is the output of the show-task command.",
      "request": "POST {{server}}/set-data-center-server\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"my_nutanix\",\n  \"username\" : \"admin\",\n  \"hostname\" : \"1.1.1.1\"\n}",
      "response": "{\n  \"tasks\" : [ {\n    \"task-name\" : \"Data Center Operation\",\n    \"task-id\" : \"01234567-89ab-cdef-b4ab-a5aefde29b2e\",\n    \"status\" : \"succeeded\",\n    \"progress-percentage\" : 100,\n    \"suppressed\" : false,\n    \"task-details\" : [ ]\n  } ]\n}"
    },
    "set-data-center-server type OCI": {
      "description": "Set any argument for a data center server of type OCI,Use the show-task command to check the progress of the task. Output below is the output of the show-task command.",
      "request": "POST {{server}}/set-data-center-server\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"my_oci\",\n  \"key_region\" : \"us-ashburn-1\"\n}",
      "response": "{\n  \"tasks\" : [ {\n    \"task-name\" : \"Data Center Operation\",\n    \"task-id\" : \"01234567-89ab-cdef-83b9-1b4cb69b0b3c\",\n    \"status\" : \"succeeded\",\n    \"progress-percentage\" : 100,\n    \"suppressed\" : false,\n    \"task-details\" : [ ]\n  } ]\n}"
    },
    "set-data-center-server type OpenStack": {
      "description": "Set any argument for a data center server of type OpenStack,Use the show-task command to check the progress of the task. Output below is the output of the show-task command.",
      "request": "POST {{server}}/set-data-center-server\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"my_openStack\",\n  \"username\" : \"domain2/username1\",\n  \"password-base64\" : \"YWRtaW4=\"\n}",
      "response": "{\n  \"tasks\" : [ {\n    \"task-name\" : \"Data Center Operation\",\n    \"task-id\" : \"01234567-89ab-cdef-b4ab-a5aefde29b2e\",\n    \"status\" : \"succeeded\",\n    \"progress-percentage\" : 100,\n    \"suppressed\" : false,\n    \"task-details\" : [ ]\n  } ]\n}"
    },
    "set-data-center-server type VMware NSX": {
      "description": "Set any argument for a data center server of type VMware NSX,Use the show-task command to check the progress of the task. Output below is the output of the show-task command.",
      "request": "POST {{server}}/set-data-center-server\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"my_nsx\",\n  \"new-name\" : \"admin_nsx\",\n  \"username\" : \"newAdmin\",\n  \"hostname\" : \"127.0.0.1\"\n}",
      "response": "{\n  \"tasks\" : [ {\n    \"task-name\" : \"Data Center Operation\",\n    \"task-id\" : \"01234567-89ab-cdef-b4ab-a5aefde29b2e\",\n    \"status\" : \"succeeded\",\n    \"progress-percentage\" : 100,\n    \"suppressed\" : false,\n    \"task-details\" : [ ]\n  } ]\n}"
    },
    "set-data-center-server type VMware NSX-T": {
      "description": "Set any argument for a data center server of type VMware NSX-T,Use the show-task command to check the progress of the task. Output below is the output of the show-task command.",
      "request": "POST {{server}}/set-data-center-server\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"my_nsxt\",\n  \"username\" : \"admin\",\n  \"hostname\" : \"1.1.1.1\"\n}",
      "response": "{\n  \"tasks\" : [ {\n    \"task-name\" : \"Data Center Operation\",\n    \"task-id\" : \"01234567-89ab-cdef-b4ab-a5aefde29b2e\",\n    \"status\" : \"succeeded\",\n    \"progress-percentage\" : 100,\n    \"suppressed\" : false,\n    \"task-details\" : [ ]\n  } ]\n}"
    },
    "set-data-center-server type vCenter": {
      "description": "Set any argument for a data center server of type vCenter,Use the show-task command to check the progress of the task. Output below is the output of the show-task command.",
      "request": "POST {{server}}/set-data-center-server\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"my_vcenter\",\n  \"username\" : \"new_admin\",\n  \"password-base64\" : \"YWRtaW4=\",\n  \"comments\" : \"vCenter server for username new_admin\",\n  \"color\" : \"red\"\n}",
      "response": "{\n  \"tasks\" : [ {\n    \"task-name\" : \"Data Center Operation\",\n    \"task-id\" : \"01234567-89ab-cdef-b4ab-a5aefde29b2e\",\n    \"status\" : \"succeeded\",\n    \"progress-percentage\" : 100,\n    \"suppressed\" : false,\n    \"task-details\" : [ ]\n  } ]\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:16.381809",
    "source_file": "set-data-center-server.html"
  }
}
```