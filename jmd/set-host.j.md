# set-host

```json
{
  "command": "set-host",
  "description": "Edit existing object using object name or uid.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/set-host",
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
        "name": "interfaces",
        "description": "",
        "type": "array",
        "required": false,
        "default": "black",
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
          "yellow"
        ]
      },
      {
        "name": "add",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "black",
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
          "yellow"
        ]
      },
      {
        "name": "name",
        "description": "Interface name.",
        "type": "string",
        "required": true
      },
      {
        "name": "subnet",
        "description": "IPv4 or IPv6 network address. If both addresses are required use subnet4 and subnet6 fields explicitly.",
        "type": "string",
        "required": true
      },
      {
        "name": "mask-length",
        "description": "IPv4 or IPv6 network mask length. If both masks are required use mask-length4 and mask-length6 fields explicitly. Instead of IPv4 mask length it is possible to specify IPv4 mask itself in subnet-mask field.",
        "type": "integer",
        "required": true
      },
      {
        "name": "color",
        "description": "Color of the object. Should be one of existing colors.",
        "type": "string",
        "required": false,
        "default": "black",
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
          "yellow"
        ]
      },
      {
        "name": "comments",
        "description": "Comments string.",
        "type": "string",
        "required": false
      },
      {
        "name": "details-level",
        "description": "The level of detail for some of the fields in the response can vary from showing only the UID value of the object to a fully detailed representation of the object.",
        "type": "string",
        "required": false,
        "default": "standard",
        "valid_values": [
          "uid",
          "standard",
          "full"
        ]
      },
      {
        "name": "ignore-warnings",
        "description": "Apply changes ignoring warnings.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "ignore-errors",
        "description": "Apply changes ignoring errors. You won't be able to publish such a changes. If ignore-warnings flag was omitted - warnings will also be ignored.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "name",
        "description": "Interface name.",
        "type": "string",
        "required": true
      },
      {
        "name": "subnet",
        "description": "IPv4 or IPv6 network address. If both addresses are required use subnet4 and subnet6 fields explicitly.",
        "type": "string",
        "required": true
      },
      {
        "name": "mask-length",
        "description": "IPv4 or IPv6 network mask length. If both masks are required use mask-length4 and mask-length6 fields explicitly. Instead of IPv4 mask length it is possible to specify IPv4 mask itself in subnet-mask field.",
        "type": "integer",
        "required": true
      },
      {
        "name": "color",
        "description": "Color of the object. Should be one of existing colors.",
        "type": "string",
        "required": false,
        "default": "black",
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
          "yellow"
        ]
      },
      {
        "name": "comments",
        "description": "Comments string.",
        "type": "string",
        "required": false
      },
      {
        "name": "details-level",
        "description": "The level of detail for some of the fields in the response can vary from showing only the UID value of the object to a fully detailed representation of the object.",
        "type": "string",
        "required": false,
        "default": "standard",
        "valid_values": [
          "uid",
          "standard",
          "full"
        ]
      },
      {
        "name": "ignore-warnings",
        "description": "Apply changes ignoring warnings.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "ignore-errors",
        "description": "Apply changes ignoring errors. You won't be able to publish such a changes. If ignore-warnings flag was omitted - warnings will also be ignored.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "remove",
        "description": "Removes from collection of values",
        "type": "string",
        "required": false
      },
      {
        "name": "name",
        "description": "Interface name.",
        "type": "string",
        "required": true
      },
      {
        "name": "subnet",
        "description": "IPv4 or IPv6 network address. If both addresses are required use subnet4 and subnet6 fields explicitly.",
        "type": "string",
        "required": true
      },
      {
        "name": "mask-length",
        "description": "IPv4 or IPv6 network mask length. If both masks are required use mask-length4 and mask-length6 fields explicitly. Instead of IPv4 mask length it is possible to specify IPv4 mask itself in subnet-mask field.",
        "type": "integer",
        "required": true
      },
      {
        "name": "color",
        "description": "Color of the object. Should be one of existing colors.",
        "type": "string",
        "required": false,
        "default": "black",
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
          "yellow"
        ]
      },
      {
        "name": "comments",
        "description": "Comments string.",
        "type": "string",
        "required": false
      },
      {
        "name": "details-level",
        "description": "The level of detail for some of the fields in the response can vary from showing only the UID value of the object to a fully detailed representation of the object.",
        "type": "string",
        "required": false,
        "default": "standard",
        "valid_values": [
          "uid",
          "standard",
          "full"
        ]
      },
      {
        "name": "ignore-warnings",
        "description": "Apply changes ignoring warnings.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "ignore-errors",
        "description": "Apply changes ignoring errors. You won't be able to publish such a changes. If ignore-warnings flag was omitted - warnings will also be ignored.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "name",
        "description": "Interface name.",
        "type": "string",
        "required": true
      },
      {
        "name": "subnet",
        "description": "IPv4 or IPv6 network address. If both addresses are required use subnet4 and subnet6 fields explicitly.",
        "type": "string",
        "required": true
      },
      {
        "name": "mask-length",
        "description": "IPv4 or IPv6 network mask length. If both masks are required use mask-length4 and mask-length6 fields explicitly. Instead of IPv4 mask length it is possible to specify IPv4 mask itself in subnet-mask field.",
        "type": "integer",
        "required": true
      },
      {
        "name": "color",
        "description": "Color of the object. Should be one of existing colors.",
        "type": "string",
        "required": false,
        "default": "black",
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
          "yellow"
        ]
      },
      {
        "name": "comments",
        "description": "Comments string.",
        "type": "string",
        "required": false
      },
      {
        "name": "details-level",
        "description": "The level of detail for some of the fields in the response can vary from showing only the UID value of the object to a fully detailed representation of the object.",
        "type": "string",
        "required": false,
        "default": "standard",
        "valid_values": [
          "uid",
          "standard",
          "full"
        ]
      },
      {
        "name": "ignore-warnings",
        "description": "Apply changes ignoring warnings.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "ignore-errors",
        "description": "Apply changes ignoring errors. You won't be able to publish such a changes. If ignore-warnings flag was omitted - warnings will also be ignored.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "ip-address",
        "description": "IPv4 or IPv6 address. If both addresses are required use ipv4-address and ipv6-address fields explicitly.",
        "type": "string",
        "required": false
      },
      {
        "name": "nat-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "false",
        "valid_values": [
          "gateway",
          "ip-address"
        ]
      },
      {
        "name": "auto-rule",
        "description": "Whether to add automatic address translation rules.",
        "type": "boolean",
        "required": true,
        "default": "false"
      },
      {
        "name": "ip-address",
        "description": "IPv4 or IPv6 address. If both addresses are required use ipv4-address and ipv6-address fields explicitly. This parameter is not required in case \"method\" parameter is \"hide\" and \"hide-behind\" parameter is \"gateway\".",
        "type": "string",
        "required": true
      },
      {
        "name": "hide-behind",
        "description": "Hide behind method. This parameter is forbidden in case \"method\" parameter is \"static\".",
        "type": "string",
        "required": false,
        "valid_values": [
          "gateway",
          "ip-address"
        ]
      },
      {
        "name": "install-on",
        "description": "Which gateway should apply the NAT translation.",
        "type": "string",
        "required": false
      },
      {
        "name": "method",
        "description": "NAT translation method.",
        "type": "string",
        "required": false,
        "valid_values": [
          "hide",
          "static"
        ]
      },
      {
        "name": "new-name",
        "description": "New name of the object.",
        "type": "string",
        "required": false
      },
      {
        "name": "host-servers",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "sparc linux",
          "windows",
          "other",
          "x86 linux",
          "sparc solaris"
        ]
      },
      {
        "name": "dns-server",
        "description": "Gets True if this server is a DNS Server.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "mail-server",
        "description": "Gets True if this server is a Mail Server.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "web-server",
        "description": "Gets True if this server is a Web Server.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "web-server-config",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "sparc linux",
          "windows",
          "other",
          "x86 linux",
          "sparc solaris"
        ]
      },
      {
        "name": "additional-ports",
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
        "name": "application-engines",
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
        "name": "listen-standard-port",
        "description": "Whether server listens to standard port.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "operating-system",
        "description": "Operating System.",
        "type": "string",
        "required": false,
        "valid_values": [
          "sparc linux",
          "windows",
          "other",
          "x86 linux",
          "sparc solaris"
        ]
      },
      {
        "name": "protected-by",
        "description": "Network object which protects this server identified by the name or UID.",
        "type": "string",
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
        "name": "groups",
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
        "name": "interfaces",
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
        "name": "subnet4",
        "description": "IPv4 network address.",
        "type": "string",
        "required": false
      },
      {
        "name": "subnet6",
        "description": "IPv6 network address.",
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
        "name": "mask-length4",
        "description": "IPv4 network mask length.",
        "type": "integer",
        "required": false
      },
      {
        "name": "mask-length6",
        "description": "IPv6 network mask length.",
        "type": "integer",
        "required": false
      },
      {
        "name": "subnet-mask",
        "description": "IPv4 network mask.",
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
        "name": "ipv4-address",
        "description": "IPv4 host address.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv6-address",
        "description": "IPv6 host address.",
        "type": "string",
        "required": false
      },
      {
        "name": "nat-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "gateway",
          "ip-address"
        ]
      },
      {
        "name": "auto-rule",
        "description": "Whether to add automatic address translation rules.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "hide-behind",
        "description": "Hide behind method. This parameter is forbidden in case \"method\" parameter is \"static\".",
        "type": "string",
        "required": false,
        "valid_values": [
          "gateway",
          "ip-address"
        ]
      },
      {
        "name": "install-on",
        "description": "Which gateway should apply the NAT translation.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv4-address",
        "description": "IPv4 address.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv6-address",
        "description": "IPv6 address.",
        "type": "string",
        "required": false
      },
      {
        "name": "method",
        "description": "NAT translation method.",
        "type": "string",
        "required": false,
        "valid_values": [
          "hide",
          "static"
        ]
      },
      {
        "name": "host-servers",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "sparc linux",
          "windows",
          "other",
          "x86 linux",
          "sparc solaris"
        ]
      },
      {
        "name": "dns-server",
        "description": "Gets True if this server is a DNS Server.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "mail-server",
        "description": "Gets True if this server is a Mail Server.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "web-server",
        "description": "Gets True if this server is a Web Server.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "web-server-config",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "sparc linux",
          "windows",
          "other",
          "x86 linux",
          "sparc solaris"
        ]
      },
      {
        "name": "additional-ports",
        "description": "Server additional ports.",
        "type": "array",
        "required": false
      },
      {
        "name": "application-engines",
        "description": "Application engines of this web server.",
        "type": "array",
        "required": false
      },
      {
        "name": "listen-standard-port",
        "description": "Whether server listens to standard port.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "operating-system",
        "description": "Operating System.",
        "type": "string",
        "required": false,
        "valid_values": [
          "sparc linux",
          "windows",
          "other",
          "x86 linux",
          "sparc solaris"
        ]
      },
      {
        "name": "protected-by",
        "description": "Network object which protects this server identified by the name or UID.",
        "type": "string",
        "required": false
      },
      {
        "name": "standard-port-number",
        "description": "Server standard port number.",
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
    "set-host": {
      "description": "",
      "request": "POST {{server}}/set-host\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"New Host 1\",\n  \"ipv4-address\" : \"192.0.2.2\",\n  \"color\" : \"green\"\n}",
      "response": ""
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:17.337163",
    "source_file": "set-host.html"
  }
}
```