# add-smart-task

```json
{
  "command": "add-smart-task",
  "description": "Create a new Smart Task. This command is available only in a Security Management environment or in Multi-Domain environment when logged into local domain.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/add-smart-task",
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
        "name": "action",
        "description": "",
        "type": "array",
        "required": true,
        "default": "The local Management Server",
        "valid_values": [
          "no attachment",
          "changes report",
          "policy installation report"
        ]
      },
      {
        "name": "send-web-request",
        "description": "",
        "type": "Object",
        "required": true
      },
      {
        "name": "url",
        "description": "URL used for the web request.",
        "type": "string",
        "required": true
      },
      {
        "name": "fingerprint",
        "description": "The SHA1 fingerprint of the URL's SSL certificate. Used to trust servers with self-signed SSL certificates.",
        "type": "string",
        "required": false
      },
      {
        "name": "override-proxy",
        "description": "Option to send to the web request via a proxy other than the Management's Server proxy (if defined).",
        "type": "boolean",
        "required": false
      },
      {
        "name": "proxy-url",
        "description": "URL of the proxy used to send the request.",
        "type": "string",
        "required": false
      },
      {
        "name": "shared-secret",
        "description": "Shared secret that can be used by the target server to identify the Management Server.The value will be sent as part of the request in the \"X-chkp-shared-secret\" header.",
        "type": "string",
        "required": false
      },
      {
        "name": "time-out",
        "description": "Web Request time-out in seconds.",
        "type": "integerDescription:",
        "required": false
      },
      {
        "name": "repository-script",
        "description": "Repository script that is executed when the trigger is fired., identified by the name or UID.",
        "type": "string",
        "required": true
      },
      {
        "name": "targets",
        "description": "Targets to execute the script on.",
        "type": "string",
        "required": false,
        "default": "The local Management Server"
      },
      {
        "name": "time-out",
        "description": "Script execution time-out in seconds.",
        "type": "integerDescription:",
        "required": false
      },
      {
        "name": "mail-settings",
        "description": "",
        "type": "Object",
        "required": true,
        "valid_values": [
          "no attachment",
          "changes report",
          "policy installation report"
        ]
      },
      {
        "name": "recipients",
        "description": "A comma separated list of recipient mail addresses.",
        "type": "string",
        "required": true
      },
      {
        "name": "sender-email",
        "description": "An email address to send the mail from.",
        "type": "string",
        "required": true
      },
      {
        "name": "subject",
        "description": "The email subject.",
        "type": "string",
        "required": true
      },
      {
        "name": "body",
        "description": "The email body.",
        "type": "string",
        "required": true
      },
      {
        "name": "attachment",
        "description": "What file should be attached to the mail.",
        "type": "string",
        "required": false,
        "valid_values": [
          "no attachment",
          "changes report",
          "policy installation report"
        ]
      },
      {
        "name": "bcc-recipients",
        "description": "A comma separated list of bcc recipient mail addresses.",
        "type": "string",
        "required": false
      },
      {
        "name": "cc-recipients",
        "description": "A comma separated list of cc recipient mail addresses.",
        "type": "string",
        "required": false
      },
      {
        "name": "smtp-server",
        "description": "The UID or the name a preconfigured SMTP server object.",
        "type": "string",
        "required": true
      },
      {
        "name": "trigger",
        "description": "Trigger type associated with the SmartTask.",
        "type": "string",
        "required": true,
        "valid_values": [
          "After Install Policy",
          "After Publish",
          "After Reject",
          "After Submit",
          "Before Approve",
          "Before Login",
          "Before Publish",
          "Before Reject",
          "Before Submit",
          "CloudGuard Controller Event"
        ]
      },
      {
        "name": "custom-data",
        "description": "Per SmartTask custom data in JSON format.When the trigger is fired, the trigger data is converted to JSON. The custom data is then concatenated to the trigger data JSON.",
        "type": "string",
        "required": false
      },
      {
        "name": "description",
        "description": "Description of the SmartTask's functionality and options.",
        "type": "string",
        "required": false
      },
      {
        "name": "enabled",
        "description": "Whether the SmartTask is enabled and will run when triggered.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "fail-open",
        "description": "If the action fails to execute, whether to treat the execution failure as an error, or continue.",
        "type": "boolean",
        "required": false,
        "default": "true"
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
        "name": "trigger",
        "description": "",
        "type": "Object",
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
        "name": "type",
        "description": "Object type.",
        "type": "string",
        "required": false
      },
      {
        "name": "action",
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
        "name": "run-script",
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
        "name": "type",
        "description": "Object type.",
        "type": "string",
        "required": false
      },
      {
        "name": "repository-script",
        "description": "",
        "type": "Object",
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
        "name": "targets",
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
        "name": "time-out",
        "description": "Script execution time-out in seconds.",
        "type": "integerDescription:",
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
        "name": "tags",
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
        "name": "send-mail",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "no attachment",
          "changes report",
          "policy installation report"
        ]
      },
      {
        "name": "uid",
        "description": "Object unique identifier.",
        "type": "string",
        "required": false
      },
      {
        "name": "mail-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "no attachment",
          "changes report",
          "policy installation report"
        ]
      },
      {
        "name": "recipients",
        "description": "A comma separated list of recipient mail addresses.",
        "type": "string",
        "required": false
      },
      {
        "name": "sender-email",
        "description": "An email address to send the mail from.",
        "type": "string",
        "required": false
      },
      {
        "name": "subject",
        "description": "The email subject.",
        "type": "string",
        "required": false
      },
      {
        "name": "body",
        "description": "The email body.",
        "type": "string",
        "required": false
      },
      {
        "name": "attachment",
        "description": "What file should be attached to the mail.",
        "type": "string",
        "required": false,
        "valid_values": [
          "no attachment",
          "changes report",
          "policy installation report"
        ]
      },
      {
        "name": "bcc-recipients",
        "description": "A comma separated list of bcc recipient mail addresses.",
        "type": "string",
        "required": false
      },
      {
        "name": "cc-recipients",
        "description": "A comma separated list of cc recipient mail addresses.",
        "type": "string",
        "required": false
      },
      {
        "name": "smtp-server",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "none",
          "ssl",
          "tls"
        ]
      },
      {
        "name": "name",
        "description": "Object name. Must be unique in the domain.",
        "type": "string",
        "required": false
      },
      {
        "name": "port",
        "description": "The SMTP port to use.",
        "type": "integer",
        "required": false
      },
      {
        "name": "server",
        "description": "The SMTP server address.",
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
        "name": "authentication",
        "description": "Does the mail server requires authentication.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "encryption",
        "description": "Encryption type.",
        "type": "string",
        "required": false,
        "valid_values": [
          "none",
          "ssl",
          "tls"
        ]
      },
      {
        "name": "type",
        "description": "Object type.",
        "type": "string",
        "required": false
      },
      {
        "name": "username",
        "description": "A username for the SMTP server.",
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
        "name": "tags",
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
        "name": "type",
        "description": "Object type.",
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
        "name": "tags",
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
        "name": "send-web-request",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "mds",
          "data domain",
          "domain",
          "global domain"
        ]
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
        "name": "url",
        "description": "URL used for the web request.",
        "type": "string",
        "required": false
      },
      {
        "name": "fingerprint",
        "description": "The SHA1 fingerprint of the URL's SSL certificate. Used to trust servers with self-signed SSL certificates.",
        "type": "string",
        "required": false
      },
      {
        "name": "override-proxy",
        "description": "Option to send to the web request via a proxy other than the Management's Server proxy (if defined).",
        "type": "boolean",
        "required": false
      },
      {
        "name": "proxy-url",
        "description": "URL of the proxy used to send the request.",
        "type": "string",
        "required": false
      },
      {
        "name": "shared-secret",
        "description": "Shared secret that can be used by the target server to identify the Management Server.The value will be sent as part of the request in the \"X-chkp-shared-secret\" header.",
        "type": "string",
        "required": false
      },
      {
        "name": "time-out",
        "description": "Web Request time-out in seconds.",
        "type": "integerDescription:",
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
        "name": "tags",
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
        "name": "custom-data",
        "description": "Per SmartTask custom data in JSON format.When the trigger is fired, the trigger data is converted to JSON. The custom data is then concatenated to the trigger data JSON.",
        "type": "string",
        "required": false
      },
      {
        "name": "description",
        "description": "Description of the SmartTask's functionality and options.",
        "type": "string",
        "required": false
      },
      {
        "name": "enabled",
        "description": "Whether the SmartTask is enabled and will run when triggered.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "fail-open",
        "description": "If the action fails to execute, whether to treat the execution failure as an error, or continue.",
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
    "add-smart-task that runs a script before publish": {
      "description": "Adds a SmartTask that will run before publish and execute the \"Validate Session Name\" script on the Management Server.Note:This example assumes a script called \"Validate Session Name\" exists in the Management's Script Repository.The Script Repository can be accessed from SmartConsole > Gateways & Servers > Scripts > Script Repository",
      "request": "POST {{server}}/add-smart-task\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"Validate Session Name Before Publish\",\n  \"trigger\" : \"Before Publish\",\n  \"description\" : \"Run a validation script that ensures that the a session name matches the expected name format as described in the Custom Data field.\",\n  \"action\" : {\n    \"run-script\" : {\n      \"repository-script\" : \"Session Name Validation Script\",\n      \"time-out\" : 30\n    }\n  },\n  \"custom-data\" : \"{\\\"session-name-format\\\": \\\"CR\\\"}\",\n  \"enabled\" : true\n}",
      "response": "{\n  \"uid\" : \"37a1a743-3f76-41cc-bc71-2ff2c0dd8da3\",\n  \"name\" : \"Validate Session Name Before Publish\",\n  \"type\" : \"smart-task\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1563808879731,\n      \"iso-8601\" : \"2019-07-22T18:21+0300\"\n    },\n    \"last-modifier\" : \"aa\",\n    \"creation-time\" : {\n      \"posix\" : 1563808879731,\n      \"iso-8601\" : \"2019-07-22T18:21+0300\"\n    },\n    \"creator\" : \"aa\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : true,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"Objects/SmartTask\",\n  \"enabled\" : true,\n  \"trigger\" : {\n    \"uid\" : \"c1ae2fc1-aeda-413a-9910-f9083f9885fa\",\n    \"name\" : \"Before Publish\",\n    \"type\" : \"smart-task-trigger\",\n    \"domain\" : {\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\",\n      \"domain-type\" : \"data domain\"\n    }\n  },\n  \"description\" : \"Run a validation script that ensures that the a session name matches the expected name format as described in the Custom Data field.\",\n  \"fail-open\" : true,\n  \"custom-data\" : \"{\\\"session-name-format\\\": \\\"CR\\\"}\",\n  \"action\" : {\n    \"run-script\" : {\n      \"repository-script\" : {\n        \"uid\" : \"ce47e4ce-7dbb-45fa-8025-b16af0fa9a53\",\n        \"name\" : \"Session Name Validation Script\",\n        \"type\" : \"Script\",\n        \"domain\" : {\n          \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n          \"name\" : \"SMC User\",\n          \"domain-type\" : \"domain\"\n        }\n      }\n    }\n  }\n}"
    },
    "add-smart-task that sends an email after submit": {
      "description": "Adds a SmartTask that will run after submit and send an email notifying the recipients of the submitted session with a change report attached.",
      "request": "POST {{server}}/add-smart-task\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"Send Mail After Submit\",\n  \"trigger\" : \"After Submit\",\n  \"description\" : \"Notifying via email about a submitted session with change report attached.\",\n  \"action\" : {\n    \"send-mail\" : {\n      \"mail-settings\" : {\n        \"subject\" : \"A session was submitted\",\n        \"recipients\" : \"recipient1@example.com,recipient2@example.com\",\n        \"sender-email\" : \"sender@example.com\",\n        \"body\" : \"Please review my session\",\n        \"attachment\" : \"changes_report\"\n      },\n      \"smtp-server\" : \"SMTP\"\n    }\n  },\n  \"enabled\" : true\n}",
      "response": "{\n  \"uid\" : \"1baf4730-6a19-424c-8f6f-93393a956b8a\",\n  \"name\" : \"Send Mail After Submit\",\n  \"type\" : \"smart-task\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1639665028017,\n      \"iso-8601\" : \"2021-12-16T16:30+0200\"\n    },\n    \"last-modifier\" : \"aa\",\n    \"creation-time\" : {\n      \"posix\" : 1639665028017,\n      \"iso-8601\" : \"2021-12-16T16:30+0200\"\n    },\n    \"creator\" : \"aa\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : true,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"Objects/SmartTask\",\n  \"enabled\" : true,\n  \"trigger\" : {\n    \"uid\" : \"4154075c-900f-40fa-8bf7-21dbf8421c44\",\n    \"name\" : \"After Submit\",\n    \"type\" : \"smart-task-trigger\",\n    \"domain\" : {\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\",\n      \"domain-type\" : \"data domain\"\n    },\n    \"icon\" : \"General/globalsNa\",\n    \"color\" : \"black\"\n  },\n  \"description\" : \"Notifying via email about a submitted session with change report attached.\",\n  \"fail-open\" : true,\n  \"custom-data\" : \"\",\n  \"action\" : {\n    \"send-mail\" : {\n      \"smtp-server\" : {\n        \"uid\" : \"26b91119-43b0-4fd5-8db0-ac051319962c\",\n        \"name\" : \"SMTP\",\n        \"type\" : \"smtp-server\",\n        \"domain\" : {\n          \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n          \"name\" : \"SMC User\",\n          \"domain-type\" : \"domain\"\n        },\n        \"meta-info\" : {\n          \"lock\" : \"locked by current session\",\n          \"validation-state\" : \"ok\",\n          \"last-modify-time\" : {\n            \"posix\" : 1639472230980,\n            \"iso-8601\" : \"2021-12-14T10:57+0200\"\n          },\n          \"last-modifier\" : \"aa\",\n          \"creation-time\" : {\n            \"posix\" : 1639472230980,\n            \"iso-8601\" : \"2021-12-14T10:57+0200\"\n          },\n          \"creator\" : \"aa\"\n        },\n        \"tags\" : [ ],\n        \"read-only\" : false,\n        \"comments\" : \"\",\n        \"color\" : \"black\",\n        \"icon\" : \"Objects/account_unit\",\n        \"server\" : \"smtp.checkpoint.com\",\n        \"port\" : 25,\n        \"username\" : \"\"\n      },\n      \"mail-settings\" : {\n        \"subject\" : \"A session was submitted\",\n        \"recipients\" : \"recipient1@example.com,recipient2@example.com\",\n        \"body\" : \"Please review my session\",\n        \"sender-email\" : \"sender@example.com\",\n        \"attachment\" : \"changes report\"\n      }\n    }\n  }\n}"
    },
    "add-smart-task that sends a web request after policy installations": {
      "description": "Adds a SmartTask that will run after install policy and send a web request to the target URL.",
      "request": "POST {{server}}/add-smart-task\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"Send Policy Installation Reports\",\n  \"description\" : \"Send policy installation results to the mail address specified in the Custom Data field using the corporate's dedicated web server.\",\n  \"enabled\" : true,\n  \"trigger\" : \"After Install Policy\",\n  \"custom-data\" : \"{\\\"mail-address\\\": \\\"example-admin@example-corp.com\\\"}\",\n  \"action\" : {\n    \"send-web-request\" : {\n      \"url\" : \"https://demo.example.com/policy-installation-reports\",\n      \"fingerprint\" : \"3FDD902286DBF130EF4CEC7939EF81060AB0FEB6\"\n    }\n  }\n}",
      "response": "{\n  \"uid\" : \"19c71ca2-3080-4617-b6ea-7c376e582bb8\",\n  \"name\" : \"Send Policy Installation Reports\",\n  \"type\" : \"smart-task\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1556717294959,\n      \"iso-8601\" : \"2019-05-01T16:28+0300\"\n    },\n    \"last-modifier\" : \"aa\",\n    \"creation-time\" : {\n      \"posix\" : 1556717294959,\n      \"iso-8601\" : \"2019-05-01T16:28+0300\"\n    },\n    \"creator\" : \"aa\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : true,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"Objects/SmartTask\",\n  \"enabled\" : true,\n  \"trigger\" : {\n    \"uid\" : \"2f98776f-1352-4947-a087-0446d8b5d93c\",\n    \"name\" : \"After Install Policy\",\n    \"type\" : \"smart-task-trigger\",\n    \"domain\" : {\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\",\n      \"domain-type\" : \"data domain\"\n    }\n  },\n  \"description\" : \"Send policy installation results to the mail address specified in the Custom Data field using the corporate's dedicated web server.\",\n  \"fail-open\" : true,\n  \"custom-data\" : \"{\\\"mail-address\\\": \\\"example-admin@example-corp.com\\\"}\",\n  \"action\" : {\n    \"web-request\" : {\n      \"url\" : \"https://demo.example.com/policy-installation-reports/\",\n      \"time-out\" : 30000\n    }\n  }\n}"
    },
    "add-smart-task that sends a web request via proxy after policy installations": {
      "description": "Adds a SmartTask that will run after install policy and send a web request to the target URL via the specified proxy.",
      "request": "POST {{server}}/add-smart-task\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"Send Policy Installation Reports via Proxy\",\n  \"description\" : \"Send policy installation results to the mail address specified in the Custom Data field using the corporate's dedicated web server.\",\n  \"enabled\" : true,\n  \"trigger\" : \"After Install Policy\",\n  \"custom-data\" : \"{\\\"mail-address\\\": \\\"example-admin@example-corp.com\\\"}\",\n  \"action\" : {\n    \"send-web-request\" : {\n      \"url\" : \"https://demo.example-corp.com/policy-installation-reports/\",\n      \"override-proxy\" : true,\n      \"proxy-url\" : \"http://proxy.example-corp.com:8080\",\n      \"shared-secret\" : \"mysharedsecret1\",\n      \"time-out\" : 60\n    }\n  }\n}",
      "response": "{\n  \"uid\" : \"19c71ca2-3080-4617-b6ea-7c376e582bb8\",\n  \"name\" : \"Send Policy Installation Reports\",\n  \"type\" : \"smart-task\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1556717294959,\n      \"iso-8601\" : \"2019-05-01T16:28+0300\"\n    },\n    \"last-modifier\" : \"aa\",\n    \"creation-time\" : {\n      \"posix\" : 1556717294959,\n      \"iso-8601\" : \"2019-05-01T16:28+0300\"\n    },\n    \"creator\" : \"aa\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : true,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"Objects/SmartTask\",\n  \"enabled\" : true,\n  \"trigger\" : {\n    \"uid\" : \"2f98776f-1352-4947-a087-0446d8b5d93c\",\n    \"name\" : \"After Install Policy\",\n    \"type\" : \"smart-task-trigger\",\n    \"domain\" : {\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\",\n      \"domain-type\" : \"data domain\"\n    }\n  },\n  \"description\" : \"Send policy installation results to the mail address specified in the Custom Data field using the corporate's dedicated web server.\",\n  \"fail-open\" : true,\n  \"custom-data\" : \"{\\\"mail-address\\\": \\\"example-admin@example-corp.com\\\"}\",\n  \"action\" : {\n    \"web-request\" : {\n      \"url\" : \"https://demo.example.com/policy-installation-reports/\",\n      \"time-out\" : 30000\n    }\n  }\n}"
    },
    "add-smart-task that runs a script after policy installations on the specified targets": {
      "description": "Adds a SmartTask that will run after policy installations and execute the \"Show Policy Status\" script on the specified targets.Note:This example assumes a script called \"Show Policy Status\" exists in the Management's Script Repository.The Script Repository can be accessed from SmartConsole > Gateways & Servers > Scripts > Script Repository",
      "request": "POST {{server}}/add-smart-task\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"Show Policy Status on Gateways\",\n  \"trigger\" : \"After Install Policy\",\n  \"description\" : \"Run policy status script on gateways after policy installations.\",\n  \"action\" : {\n    \"run-script\" : {\n      \"repository-script\" : \"Show Policy Status\",\n      \"targets\" : [ \"Corporate-Gateway\", \"BranchOffice\" ],\n      \"time-out\" : 120\n    }\n  },\n  \"enabled\" : true\n}",
      "response": "{\n  \"uid\" : \"37a1a743-3f76-41cc-bc71-2ff2c0dd8da3\",\n  \"name\" : \"Validate Session Name Before Publish\",\n  \"type\" : \"smart-task\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1563808879731,\n      \"iso-8601\" : \"2019-07-22T18:21+0300\"\n    },\n    \"last-modifier\" : \"aa\",\n    \"creation-time\" : {\n      \"posix\" : 1563808879731,\n      \"iso-8601\" : \"2019-07-22T18:21+0300\"\n    },\n    \"creator\" : \"aa\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : true,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"Objects/SmartTask\",\n  \"enabled\" : true,\n  \"trigger\" : {\n    \"uid\" : \"c1ae2fc1-aeda-413a-9910-f9083f9885fa\",\n    \"name\" : \"Before Publish\",\n    \"type\" : \"smart-task-trigger\",\n    \"domain\" : {\n      \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n      \"name\" : \"Check Point Data\",\n      \"domain-type\" : \"data domain\"\n    }\n  },\n  \"description\" : \"Run a validation script that ensures that the a session name matches the expected name format as described in the Custom Data field.\",\n  \"fail-open\" : true,\n  \"custom-data\" : \"{\\\"session-name-format\\\": \\\"CR\\\"}\",\n  \"action\" : {\n    \"run-script\" : {\n      \"repository-script\" : {\n        \"uid\" : \"ce47e4ce-7dbb-45fa-8025-b16af0fa9a53\",\n        \"name\" : \"Session Name Validation Script\",\n        \"type\" : \"Script\",\n        \"domain\" : {\n          \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n          \"name\" : \"SMC User\",\n          \"domain-type\" : \"domain\"\n        }\n      }\n    }\n  }\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:09.523002",
    "source_file": "add-smart-task.html"
  }
}
```