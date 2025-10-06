# show-vpn-community-star

```json
{
  "command": "show-vpn-community-star",
  "description": "Retrieve existing object using object name or uid.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/show-vpn-community-star",
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
        "name": "center-gateways",
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
        "name": "disable-nat",
        "description": "Indicates whether to disable NAT inside the VPN Community.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "disable-nat-on",
        "description": "Indicates on which gateways to disable NAT inside the VPN Community.",
        "type": "string",
        "required": false,
        "valid_values": [
          "satellite gateways only",
          "both center and satellite gateways"
        ]
      },
      {
        "name": "encrypted-traffic",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "satellite gateways only",
          "both center and satellite gateways"
        ]
      },
      {
        "name": "enabled",
        "description": "Indicates whether to accept all encrypted traffic.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "community-members",
        "description": "Indicates on which community members to accept all encrypted traffic.",
        "type": "string",
        "required": false,
        "valid_values": [
          "satellite gateways only",
          "both center and satellite gateways"
        ]
      },
      {
        "name": "encryption-method",
        "description": "The encryption method to be used.",
        "type": "string",
        "required": false,
        "valid_values": [
          "prefer ikev2 but support ikev1",
          "ikev2 only",
          "ikev1 for ipv4 and ikev2 for ipv6 only"
        ]
      },
      {
        "name": "encryption-suite",
        "description": "The encryption suite to be used.",
        "type": "string",
        "required": false,
        "valid_values": [
          "suite-b-gcm-256",
          "custom",
          "vpn b",
          "vpn a",
          "suite-b-gcm-128"
        ]
      },
      {
        "name": "excluded-services",
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
        "name": "granular-encryptions",
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
        "name": "internal-gateway",
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
        "name": "external-gateway",
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
        "name": "encryption-method",
        "description": "The encryption method to be used.",
        "type": "string",
        "required": false,
        "valid_values": [
          "prefer ikev2 but support ikev1",
          "ikev2 only",
          "ikev1 for ipv4 and ikev2 for ipv6 only"
        ]
      },
      {
        "name": "encryption-suite",
        "description": "The encryption suite to be used.",
        "type": "string",
        "required": false,
        "valid_values": [
          "suite-b-gcm-256",
          "custom",
          "vpn b",
          "vpn a",
          "suite-b-gcm-128"
        ]
      },
      {
        "name": "ike-phase-1",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "cast",
          "aes-256",
          "des",
          "aes-128",
          "3des",
          "aes-gcm-128",
          "aes-gcm-256"
        ]
      },
      {
        "name": "encryption-algorithm",
        "description": "The encryption algorithm to be used.",
        "type": "string",
        "required": false,
        "valid_values": [
          "cast",
          "aes-256",
          "des",
          "aes-128",
          "3des",
          "aes-gcm-128",
          "aes-gcm-256"
        ]
      },
      {
        "name": "data-integrity",
        "description": "The hash algorithm to be used.",
        "type": "string",
        "required": false,
        "valid_values": [
          "aes-xcbc",
          "sha1",
          "sha256",
          "sha384",
          "sha512",
          "md5"
        ]
      },
      {
        "name": "diffie-hellman-group",
        "description": "The Diffie-Hellman group to be used.",
        "type": "string",
        "required": false,
        "valid_values": [
          "group-1",
          "group-2",
          "group-5",
          "group-14",
          "group-15",
          "group-16",
          "group-17",
          "group-18",
          "group-19",
          "group-20",
          "group-21",
          "group-24"
        ]
      },
      {
        "name": "use-standard-proposal",
        "description": "Indicates whether to use a proposal with a single Diffie-Hellman group.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "use-multiple-key-exchanges",
        "description": "Indicates whether to use a proposal with Multiple Key Exchanges.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "multiple-key-exchanges",
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
        "name": "key-exchange-methods",
        "description": "Key-Exchange methods to use. Can contain only Diffie-Hellman groups.",
        "type": "array",
        "required": false
      },
      {
        "name": "additional-key-exchange-1-methods",
        "description": "Additional Key-Exchange 1 methods to use.",
        "type": "array",
        "required": false
      },
      {
        "name": "additional-key-exchange-2-methods",
        "description": "Additional Key-Exchange 2 methods to use.",
        "type": "array",
        "required": false
      },
      {
        "name": "additional-key-exchange-3-methods",
        "description": "Additional Key-Exchange 3 methods to use.",
        "type": "array",
        "required": false
      },
      {
        "name": "additional-key-exchange-4-methods",
        "description": "Additional Key-Exchange 4 methods to use.",
        "type": "array",
        "required": false
      },
      {
        "name": "additional-key-exchange-5-methods",
        "description": "Additional Key-Exchange 5 methods to use.",
        "type": "array",
        "required": false
      },
      {
        "name": "additional-key-exchange-6-methods",
        "description": "Additional Key-Exchange 6 methods to use.",
        "type": "array",
        "required": false
      },
      {
        "name": "additional-key-exchange-7-methods",
        "description": "Additional Key-Exchange 7 methods to use.",
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
        "name": "ike-p1-rekey-time",
        "description": "Indicates the time interval for IKE phase 1 renegotiation.",
        "type": "integer",
        "required": false
      },
      {
        "name": "ike-phase-2",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "cast",
          "aes-gcm-256",
          "cast-40",
          "aes-256",
          "des",
          "aes-128",
          "3des",
          "des-40cp",
          "aes-gcm-128",
          "none"
        ]
      },
      {
        "name": "encryption-algorithm",
        "description": "The encryption algorithm to be used.",
        "type": "string",
        "required": false,
        "valid_values": [
          "cast",
          "aes-gcm-256",
          "cast-40",
          "aes-256",
          "des",
          "aes-128",
          "3des",
          "des-40cp",
          "aes-gcm-128",
          "none"
        ]
      },
      {
        "name": "data-integrity",
        "description": "The hash algorithm to be used.",
        "type": "string",
        "required": false,
        "valid_values": [
          "aes-xcbc",
          "sha1",
          "sha256",
          "sha384",
          "sha512",
          "md5"
        ]
      },
      {
        "name": "ike-p2-use-pfs",
        "description": "Indicates whether Perfect Forward Secrecy (PFS) is being used for IKE phase 2.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "ike-p2-pfs-dh-grp",
        "description": "The Diffie-Hellman group to be used.",
        "type": "string",
        "required": false,
        "valid_values": [
          "group-1",
          "group-2",
          "group-5",
          "group-14",
          "group-15",
          "group-16",
          "group-17",
          "group-18",
          "group-19",
          "group-20",
          "group-21",
          "group-24"
        ]
      },
      {
        "name": "use-standard-proposal",
        "description": "Indicates whether to use a proposal with a single Diffie-Hellman group when PFS is enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "use-multiple-key-exchanges",
        "description": "Indicates whether to use a proposal with Multiple Key Exchanges when PFS is enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "multiple-key-exchanges",
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
        "name": "key-exchange-methods",
        "description": "Key-Exchange methods to use. Can contain only Diffie-Hellman groups.",
        "type": "array",
        "required": false
      },
      {
        "name": "additional-key-exchange-1-methods",
        "description": "Additional Key-Exchange 1 methods to use.",
        "type": "array",
        "required": false
      },
      {
        "name": "additional-key-exchange-2-methods",
        "description": "Additional Key-Exchange 2 methods to use.",
        "type": "array",
        "required": false
      },
      {
        "name": "additional-key-exchange-3-methods",
        "description": "Additional Key-Exchange 3 methods to use.",
        "type": "array",
        "required": false
      },
      {
        "name": "additional-key-exchange-4-methods",
        "description": "Additional Key-Exchange 4 methods to use.",
        "type": "array",
        "required": false
      },
      {
        "name": "additional-key-exchange-5-methods",
        "description": "Additional Key-Exchange 5 methods to use.",
        "type": "array",
        "required": false
      },
      {
        "name": "additional-key-exchange-6-methods",
        "description": "Additional Key-Exchange 6 methods to use.",
        "type": "array",
        "required": false
      },
      {
        "name": "additional-key-exchange-7-methods",
        "description": "Additional Key-Exchange 7 methods to use.",
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
        "name": "ike-p2-rekey-time",
        "description": "Indicates the time interval for IKE phase 2 renegotiation.",
        "type": "integer",
        "required": false
      },
      {
        "name": "ike-phase-1",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "cast",
          "aes-256",
          "des",
          "aes-128",
          "3des",
          "aes-gcm-128",
          "aes-gcm-256"
        ]
      },
      {
        "name": "encryption-algorithm",
        "description": "The encryption algorithm to be used.",
        "type": "string",
        "required": false,
        "valid_values": [
          "cast",
          "aes-256",
          "des",
          "aes-128",
          "3des",
          "aes-gcm-128",
          "aes-gcm-256"
        ]
      },
      {
        "name": "data-integrity",
        "description": "The hash algorithm to be used.",
        "type": "string",
        "required": false,
        "valid_values": [
          "aes-xcbc",
          "sha1",
          "sha256",
          "sha384",
          "sha512",
          "md5"
        ]
      },
      {
        "name": "diffie-hellman-group",
        "description": "The Diffie-Hellman group to be used.",
        "type": "string",
        "required": false,
        "valid_values": [
          "group-1",
          "group-2",
          "group-5",
          "group-14",
          "group-15",
          "group-16",
          "group-17",
          "group-18",
          "group-19",
          "group-20",
          "group-21",
          "group-24"
        ]
      },
      {
        "name": "use-standard-proposal",
        "description": "Indicates whether to use a proposal with a single Diffie-Hellman group.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "use-multiple-key-exchanges",
        "description": "Indicates whether to use a proposal with Multiple Key Exchanges.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "multiple-key-exchanges",
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
        "name": "key-exchange-methods",
        "description": "Key-Exchange methods to use. Can contain only Diffie-Hellman groups.",
        "type": "array",
        "required": false
      },
      {
        "name": "additional-key-exchange-1-methods",
        "description": "Additional Key-Exchange 1 methods to use.",
        "type": "array",
        "required": false
      },
      {
        "name": "additional-key-exchange-2-methods",
        "description": "Additional Key-Exchange 2 methods to use.",
        "type": "array",
        "required": false
      },
      {
        "name": "additional-key-exchange-3-methods",
        "description": "Additional Key-Exchange 3 methods to use.",
        "type": "array",
        "required": false
      },
      {
        "name": "additional-key-exchange-4-methods",
        "description": "Additional Key-Exchange 4 methods to use.",
        "type": "array",
        "required": false
      },
      {
        "name": "additional-key-exchange-5-methods",
        "description": "Additional Key-Exchange 5 methods to use.",
        "type": "array",
        "required": false
      },
      {
        "name": "additional-key-exchange-6-methods",
        "description": "Additional Key-Exchange 6 methods to use.",
        "type": "array",
        "required": false
      },
      {
        "name": "additional-key-exchange-7-methods",
        "description": "Additional Key-Exchange 7 methods to use.",
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
        "name": "ike-p1-rekey-time",
        "description": "Indicates the time interval for IKE phase 1 renegotiation.",
        "type": "integer",
        "required": false
      },
      {
        "name": "ike-phase-2",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "cast",
          "aes-gcm-256",
          "cast-40",
          "aes-256",
          "des",
          "aes-128",
          "3des",
          "des-40cp",
          "aes-gcm-128",
          "none"
        ]
      },
      {
        "name": "encryption-algorithm",
        "description": "The encryption algorithm to be used.",
        "type": "string",
        "required": false,
        "valid_values": [
          "cast",
          "aes-gcm-256",
          "cast-40",
          "aes-256",
          "des",
          "aes-128",
          "3des",
          "des-40cp",
          "aes-gcm-128",
          "none"
        ]
      },
      {
        "name": "data-integrity",
        "description": "The hash algorithm to be used.",
        "type": "string",
        "required": false,
        "valid_values": [
          "aes-xcbc",
          "sha1",
          "sha256",
          "sha384",
          "sha512",
          "md5"
        ]
      },
      {
        "name": "ike-p2-use-pfs",
        "description": "Indicates whether Perfect Forward Secrecy (PFS) is being used for IKE phase 2.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "ike-p2-pfs-dh-grp",
        "description": "The Diffie-Hellman group to be used.",
        "type": "string",
        "required": false,
        "valid_values": [
          "group-1",
          "group-2",
          "group-5",
          "group-14",
          "group-15",
          "group-16",
          "group-17",
          "group-18",
          "group-19",
          "group-20",
          "group-21",
          "group-24"
        ]
      },
      {
        "name": "use-standard-proposal",
        "description": "Indicates whether to use a proposal with a single Diffie-Hellman group when PFS is enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "use-multiple-key-exchanges",
        "description": "Indicates whether to use a proposal with Multiple Key Exchanges when PFS is enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "multiple-key-exchanges",
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
        "name": "key-exchange-methods",
        "description": "Key-Exchange methods to use. Can contain only Diffie-Hellman groups.",
        "type": "array",
        "required": false
      },
      {
        "name": "additional-key-exchange-1-methods",
        "description": "Additional Key-Exchange 1 methods to use.",
        "type": "array",
        "required": false
      },
      {
        "name": "additional-key-exchange-2-methods",
        "description": "Additional Key-Exchange 2 methods to use.",
        "type": "array",
        "required": false
      },
      {
        "name": "additional-key-exchange-3-methods",
        "description": "Additional Key-Exchange 3 methods to use.",
        "type": "array",
        "required": false
      },
      {
        "name": "additional-key-exchange-4-methods",
        "description": "Additional Key-Exchange 4 methods to use.",
        "type": "array",
        "required": false
      },
      {
        "name": "additional-key-exchange-5-methods",
        "description": "Additional Key-Exchange 5 methods to use.",
        "type": "array",
        "required": false
      },
      {
        "name": "additional-key-exchange-6-methods",
        "description": "Additional Key-Exchange 6 methods to use.",
        "type": "array",
        "required": false
      },
      {
        "name": "additional-key-exchange-7-methods",
        "description": "Additional Key-Exchange 7 methods to use.",
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
        "name": "ike-p2-rekey-time",
        "description": "Indicates the time interval for IKE phase 2 renegotiation.",
        "type": "integer",
        "required": false
      },
      {
        "name": "link-selection-mode",
        "description": "Link Selection Mode.",
        "type": "string",
        "required": false,
        "valid_values": [
          "enhanced",
          "legacy"
        ]
      },
      {
        "name": "mep",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "closest gateway to source",
          "closest gateway to destination",
          "random selection",
          "manual"
        ]
      },
      {
        "name": "enabled",
        "description": "Enable center gateways as Multiple Entry Points.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "entry-point-selection-mechanism",
        "description": "The method by which the entry point gateway will be chosen from the gateways in the center.",
        "type": "string",
        "required": false,
        "valid_values": [
          "closest gateway to source",
          "closest gateway to destination",
          "random selection",
          "manual"
        ]
      },
      {
        "name": "entry-point-final-selection-mechanism",
        "description": "The method by which the final entry point gateway will be chosen when the chosen mechanism returns more than one optional entry point.",
        "type": "string",
        "required": false,
        "valid_values": [
          "random selection",
          "first to respond"
        ]
      },
      {
        "name": "tracking",
        "description": "Tracking option for the MEP.",
        "type": "string",
        "required": false,
        "valid_values": [
          "none",
          "log",
          "popup alert",
          "mail alert",
          "snmp trap alert",
          "user defined alert no.1",
          "user defined alert no.2",
          "user defined alert no.3"
        ]
      },
      {
        "name": "default-priority-rule",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "satellite-gateways",
        "description": "Collection of satellite VPN Gateway and VPN Device objects identified by the name or UID. Level of details in the output corresponds to the number of details for search. This table shows the level of details in the Standard level.",
        "type": "array",
        "required": false
      },
      {
        "name": "first-priority-center-gateways",
        "description": "Collection of first priority center VPN Gateway and VPN Device objects identified by the name or UID. Level of details in the output corresponds to the number of details for search. This table shows the level of details in the Standard level.",
        "type": "array",
        "required": false
      },
      {
        "name": "second-priority-center-gateways",
        "description": "Collection of second priority center VPN Gateway and VPN Device objects identified by the name or UID. Level of details in the output corresponds to the number of details for search. This table shows the level of details in the Standard level.",
        "type": "array",
        "required": false
      },
      {
        "name": "third-priority-center-gateways",
        "description": "Collection of third priority center VPN Gateway and VPN Device objects identified by the name or UID. Level of details in the output corresponds to the number of details for search. This table shows the level of details in the Standard level.",
        "type": "array",
        "required": false
      },
      {
        "name": "exception-priority-rules",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "satellite-gateways",
        "description": "Collection of satellite VPN Gateway and VPN Device objects identified by the name or UID. Level of details in the output corresponds to the number of details for search. This table shows the level of details in the Standard level.",
        "type": "array",
        "required": false
      },
      {
        "name": "first-priority-center-gateways",
        "description": "Collection of first priority center VPN Gateway and VPN Device objects identified by the name or UID. Level of details in the output corresponds to the number of details for search. This table shows the level of details in the Standard level.",
        "type": "array",
        "required": false
      },
      {
        "name": "second-priority-center-gateways",
        "description": "Collection of second priority center VPN Gateway and VPN Device objects identified by the name or UID. Level of details in the output corresponds to the number of details for search. This table shows the level of details in the Standard level.",
        "type": "array",
        "required": false
      },
      {
        "name": "third-priority-center-gateways",
        "description": "Collection of third priority center VPN Gateway and VPN Device objects identified by the name or UID. Level of details in the output corresponds to the number of details for search. This table shows the level of details in the Standard level.",
        "type": "array",
        "required": false
      },
      {
        "name": "mesh-center-gateways",
        "description": "Indicates whether the meshed community is in center.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "override-interfaces",
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
        "name": "gateway",
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
        "name": "interfaces",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "active",
          "backup"
        ]
      },
      {
        "name": "interface-name",
        "description": "The name of the interface.",
        "type": "string",
        "required": false
      },
      {
        "name": "next-hop-ip",
        "description": "The IP address of the next hop.",
        "type": "string",
        "required": false
      },
      {
        "name": "static-nat-ip",
        "description": "The NATed IPv4 address that hides the source IPv4 address of outgoing connections (applies only to IPv4).",
        "type": "string",
        "required": false
      },
      {
        "name": "priority",
        "description": "Priority of a 'Backup' interface.",
        "type": "integer",
        "required": false
      },
      {
        "name": "redundancy-mode",
        "description": "Interface redundancy mode (Active/Backup).",
        "type": "string",
        "required": false,
        "valid_values": [
          "active",
          "backup"
        ]
      },
      {
        "name": "ip-version",
        "description": "The IP version of the interface's IP address (IPv4/IPv6).",
        "type": "string",
        "required": false,
        "valid_values": [
          "ipv4",
          "ipv6"
        ]
      },
      {
        "name": "override-vpn-domains",
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
        "name": "gateway",
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
        "name": "vpn-domain",
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
        "name": "permanent-tunnels",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "on all tunnels in the community",
          "on all tunnels of specific gateways",
          "on specific tunnels in the community",
          "off"
        ]
      },
      {
        "name": "set-permanent-tunnels",
        "description": "Indicates which tunnels to set as permanent.",
        "type": "string",
        "required": false,
        "valid_values": [
          "on all tunnels in the community",
          "on all tunnels of specific gateways",
          "on specific tunnels in the community",
          "off"
        ]
      },
      {
        "name": "gateways",
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
        "name": "gateway",
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
        "name": "track-options",
        "description": "Indicates whether to use the community track options or to override track options for the permanent tunnels.",
        "type": "string",
        "required": false,
        "valid_values": [
          "according to community track options",
          "override track options"
        ]
      },
      {
        "name": "override-tunnel-down-track",
        "description": "Gateway tunnel down track option. Relevant only if the track-options is set to 'override track options'.",
        "type": "string",
        "required": false,
        "valid_values": [
          "none",
          "log",
          "popup alert",
          "mail alert",
          "snmp trap alert",
          "user defined alert no.1",
          "user defined alert no.2",
          "user defined alert no.3"
        ]
      },
      {
        "name": "override-tunnel-up-track",
        "description": "Gateway tunnel up track option. Relevant only if the track-options is set to 'override track options'.",
        "type": "string",
        "required": false,
        "valid_values": [
          "none",
          "log",
          "popup alert",
          "mail alert",
          "snmp trap alert",
          "user defined alert no.1",
          "user defined alert no.2",
          "user defined alert no.3"
        ]
      },
      {
        "name": "tunnels",
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
        "name": "first-tunnel-endpoint",
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
        "name": "second-tunnel-endpoint",
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
        "name": "track-options",
        "description": "Indicates whether to use the community track options or to override track options for the permanent tunnels.",
        "type": "string",
        "required": false,
        "valid_values": [
          "according to community track options",
          "override track options"
        ]
      },
      {
        "name": "override-tunnel-down-track",
        "description": "Gateway tunnel down track option. Relevant only if the track-options is set to 'override track options'.",
        "type": "string",
        "required": false,
        "valid_values": [
          "none",
          "log",
          "popup alert",
          "mail alert",
          "snmp trap alert",
          "user defined alert no.1",
          "user defined alert no.2",
          "user defined alert no.3"
        ]
      },
      {
        "name": "override-tunnel-up-track",
        "description": "Gateway tunnel up track option. Relevant only if the track-options is set to 'override track options'.",
        "type": "string",
        "required": false,
        "valid_values": [
          "none",
          "log",
          "popup alert",
          "mail alert",
          "snmp trap alert",
          "user defined alert no.1",
          "user defined alert no.2",
          "user defined alert no.3"
        ]
      },
      {
        "name": "rim",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "none",
          "log",
          "popup alert",
          "mail alert",
          "snmp trap alert",
          "user defined alert no.1",
          "user defined alert no.2",
          "user defined alert no.3"
        ]
      },
      {
        "name": "enabled",
        "description": "Indicates whether Route Injection Mechanism is enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "enable-on-center-gateways",
        "description": "Indicates whether to enable automatic Route Injection Mechanism on center gateways.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "enable-on-satellite-gateways",
        "description": "Indicates whether to enable automatic Route Injection Mechanism on satellite gateways.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "route-injection-track",
        "description": "Route injection track method.",
        "type": "string",
        "required": false,
        "valid_values": [
          "none",
          "log",
          "popup alert",
          "mail alert",
          "snmp trap alert",
          "user defined alert no.1",
          "user defined alert no.2",
          "user defined alert no.3"
        ]
      },
      {
        "name": "tunnel-down-track",
        "description": "Permanent tunnel down track method.",
        "type": "string",
        "required": false,
        "valid_values": [
          "none",
          "log",
          "popup alert",
          "mail alert",
          "snmp trap alert",
          "user defined alert no.1",
          "user defined alert no.2",
          "user defined alert no.3"
        ]
      },
      {
        "name": "tunnel-up-track",
        "description": "VPN community permanent tunnels down track option.",
        "type": "string",
        "required": false,
        "valid_values": [
          "none",
          "log",
          "popup alert",
          "mail alert",
          "snmp trap alert",
          "user defined alert no.1",
          "user defined alert no.2",
          "user defined alert no.3"
        ]
      },
      {
        "name": "routing-mode",
        "description": "VPN Community Routing Mode.",
        "type": "string",
        "required": false,
        "valid_values": [
          "domain_based",
          "route_based"
        ]
      },
      {
        "name": "satellite-gateways",
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
        "name": "shared-secrets",
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
        "name": "external-gateway",
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
        "name": "tunnel-granularity",
        "description": "VPN tunnel sharing option to be used.",
        "type": "string",
        "required": false,
        "valid_values": [
          "per_host",
          "per_subnet",
          "universal"
        ]
      },
      {
        "name": "use-shared-secret",
        "description": "Indicates whether the shared secret should be used for all external gateways.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "vpn-routing",
        "description": "Enable VPN routing to satellites.",
        "type": "string",
        "required": false,
        "valid_values": [
          "to center only",
          "to center and to other satellites",
          "to center other satellites and internet"
        ]
      },
      {
        "name": "wire-mode",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "allow-uninspected-encrypted-traffic",
        "description": "Allow uninspected encrypted traffic between Wire mode interfaces of this Community members.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "allow-uninspected-encrypted-routing",
        "description": "Allow members to route uninspected encrypted traffic in VPN routing configurations.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "advanced-properties",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "support-ip-compression",
        "description": "Indicates whether to support IP compression.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "use-aggressive-mode",
        "description": "Indicates whether to use aggressive mode.",
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
    "show-vpn-community-star": {
      "description": "Displays a VPN Star Community",
      "request": "POST {{server}}/show-vpn-community-star\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"vpnCommunityStar\"\n}",
      "response": "{\n  \"uid\" : \"5d5ee284-dbe7-4bbc-ada4-2893d5680bc7\",\n  \"name\" : \"vpnCommunityStar\",\n  \"type\" : \"vpn-community-star\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1736889073061,\n      \"iso-8601\" : \"2025-01-14T23:11+0200\"\n    },\n    \"last-modifier\" : \"WEB_API\",\n    \"creation-time\" : {\n      \"posix\" : 1736887783809,\n      \"iso-8601\" : \"2025-01-14T22:49+0200\"\n    },\n    \"creator\" : \"WEB_API\"\n  },\n  \"available-actions\" : {\n    \"edit\" : \"true\",\n    \"delete\" : \"true\",\n    \"clone\" : \"not_supported\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : false,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"VPNCommunities/Star\",\n  \"use-shared-secret\" : false,\n  \"tunnel-granularity\" : \"per_subnet\",\n  \"encryption-method\" : \"ikev2 only\",\n  \"encryption-suite\" : \"custom\",\n  \"ike-phase-1\" : {\n    \"use-standard-proposal\" : true,\n    \"use-multiple-key-exchanges\" : false,\n    \"multiple-key-exchanges\" : {\n      \"uid\" : \"3edc642d-f613-4d39-b1a8-d38603cf7fd5\",\n      \"name\" : \"Default Multiple Key Exchanges\",\n      \"type\" : \"multiple-key-exchanges\",\n      \"domain\" : {\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\",\n        \"domain-type\" : \"data domain\"\n      },\n      \"meta-info\" : {\n        \"lock\" : \"unlocked\",\n        \"validation-state\" : \"ok\",\n        \"last-modify-time\" : {\n          \"posix\" : 1734364762484,\n          \"iso-8601\" : \"2024-12-16T17:59+0200\"\n        },\n        \"last-modifier\" : \"System\",\n        \"creation-time\" : {\n          \"posix\" : 1734364762484,\n          \"iso-8601\" : \"2024-12-16T17:59+0200\"\n        },\n        \"creator\" : \"System\"\n      },\n      \"available-actions\" : {\n        \"edit\" : \"false\",\n        \"delete\" : \"false\",\n        \"clone\" : \"true\"\n      },\n      \"tags\" : [ ],\n      \"read-only\" : true,\n      \"comments\" : \"Default Multiple Key Exchanges object contains DH Group 15 for first key-exchnage-method and Kyber 768 for additional-key-exchange-1-method\",\n      \"color\" : \"black\",\n      \"icon\" : \"General/globalsNa\",\n      \"key-exchange-methods\" : [ \"group-15\" ],\n      \"additional-key-exchange-1-methods\" : [ \"kyber-768\" ],\n      \"additional-key-exchange-2-methods\" : [ ],\n      \"additional-key-exchange-3-methods\" : [ ],\n      \"additional-key-exchange-4-methods\" : [ ],\n      \"additional-key-exchange-5-methods\" : [ ],\n      \"additional-key-exchange-6-methods\" : [ ],\n      \"additional-key-exchange-7-methods\" : [ ]\n    },\n    \"encryption-algorithm\" : \"aes-256\",\n    \"diffie-hellman-group\" : \"group-15\",\n    \"ike-p1-rekey-time\" : 1440,\n    \"data-integrity\" : \"sha384\"\n  },\n  \"ike-phase-2\" : {\n    \"use-standard-proposal\" : true,\n    \"use-multiple-key-exchanges\" : false,\n    \"multiple-key-exchanges\" : {\n      \"uid\" : \"3edc642d-f613-4d39-b1a8-d38603cf7fd5\",\n      \"name\" : \"Default Multiple Key Exchanges\",\n      \"type\" : \"multiple-key-exchanges\",\n      \"domain\" : {\n        \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n        \"name\" : \"Check Point Data\",\n        \"domain-type\" : \"data domain\"\n      },\n      \"meta-info\" : {\n        \"lock\" : \"unlocked\",\n        \"validation-state\" : \"ok\",\n        \"last-modify-time\" : {\n          \"posix\" : 1734364762484,\n          \"iso-8601\" : \"2024-12-16T17:59+0200\"\n        },\n        \"last-modifier\" : \"System\",\n        \"creation-time\" : {\n          \"posix\" : 1734364762484,\n          \"iso-8601\" : \"2024-12-16T17:59+0200\"\n        },\n        \"creator\" : \"System\"\n      },\n      \"available-actions\" : {\n        \"edit\" : \"false\",\n        \"delete\" : \"false\",\n        \"clone\" : \"true\"\n      },\n      \"tags\" : [ ],\n      \"read-only\" : true,\n      \"comments\" : \"Default Multiple Key Exchanges object contains DH Group 15 for first key-exchnage-method and Kyber 768 for additional-key-exchange-1-method\",\n      \"color\" : \"black\",\n      \"icon\" : \"General/globalsNa\",\n      \"key-exchange-methods\" : [ \"group-15\" ],\n      \"additional-key-exchange-1-methods\" : [ \"kyber-768\" ],\n      \"additional-key-exchange-2-methods\" : [ ],\n      \"additional-key-exchange-3-methods\" : [ ],\n      \"additional-key-exchange-4-methods\" : [ ],\n      \"additional-key-exchange-5-methods\" : [ ],\n      \"additional-key-exchange-6-methods\" : [ ],\n      \"additional-key-exchange-7-methods\" : [ ]\n    },\n    \"encryption-algorithm\" : \"aes-gcm-128\",\n    \"ike-p2-pfs-dh-grp\" : \"group-15\",\n    \"ike-p2-use-pfs\" : false,\n    \"ike-p2-rekey-time\" : 3600,\n    \"data-integrity\" : \"sha384\"\n  },\n  \"link-selection-mode\" : \"legacy\",\n  \"override-interfaces\" : [ ],\n  \"disable-nat\" : false,\n  \"excluded-services\" : [ ],\n  \"wire-mode\" : {\n    \"allow-uninspected-encrypted-traffic\" : false,\n    \"allow-uninspected-encrypted-routing\" : false\n  },\n  \"permanent-tunnels\" : {\n    \"set-permanent-tunnels\" : \"off\",\n    \"tunnel-down-track\" : \"log\",\n    \"tunnel-up-track\" : \"log\",\n    \"gateways\" : [ ],\n    \"tunnels\" : [ ],\n    \"rim\" : {\n      \"enabled\" : false,\n      \"enable-on-center-gateways\" : true,\n      \"enable-on-satellite-gateways\" : false,\n      \"center-gw-costumer-editable-script-exec\" : false,\n      \"satellite-gw-costumer-editable-script-exec\" : false,\n      \"route-injection-track\" : \"log\"\n    }\n  },\n  \"routing-mode\" : \"domain_based\",\n  \"center-gateways\" : [ {\n    \"uid\" : \"cfb98d59-713d-463b-8cbb-af463de8e293\",\n    \"name\" : \"centerGW4\",\n    \"type\" : \"simple-gateway\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"icon\" : \"NetworkObjects/gateway\",\n    \"color\" : \"black\"\n  }, {\n    \"uid\" : \"cce61c09-6319-4219-a487-134fd0a4e45b\",\n    \"name\" : \"centerGW2\",\n    \"type\" : \"simple-gateway\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"icon\" : \"NetworkObjects/gateway\",\n    \"color\" : \"black\"\n  }, {\n    \"uid\" : \"72ad02ec-b735-435b-b02b-1c45bacdaa85\",\n    \"name\" : \"centerGW3\",\n    \"type\" : \"simple-gateway\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"icon\" : \"NetworkObjects/gateway\",\n    \"color\" : \"black\"\n  }, {\n    \"uid\" : \"184c53e4-6fed-450a-9e79-baac108703b2\",\n    \"name\" : \"centerGW1\",\n    \"type\" : \"simple-gateway\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"icon\" : \"NetworkObjects/gateway\",\n    \"color\" : \"black\"\n  } ],\n  \"satellite-gateways\" : [ {\n    \"uid\" : \"e0d0c327-43a9-4e1e-971b-6ee83b78105a\",\n    \"name\" : \"satGW1\",\n    \"type\" : \"simple-gateway\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"icon\" : \"NetworkObjects/gateway\",\n    \"color\" : \"black\"\n  }, {\n    \"uid\" : \"7e572d86-19e8-49ca-88d3-baad72a04c0f\",\n    \"name\" : \"satGW2\",\n    \"type\" : \"simple-gateway\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"icon\" : \"NetworkObjects/gateway\",\n    \"color\" : \"black\"\n  }, {\n    \"uid\" : \"62a2e2cf-8372-4ac7-bd27-f268eae725ca\",\n    \"name\" : \"satGW3\",\n    \"type\" : \"simple-gateway\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"icon\" : \"NetworkObjects/gateway\",\n    \"color\" : \"black\"\n  } ],\n  \"mesh-center-gateways\" : false,\n  \"disable-nat-on\" : \"both center and satellite gateways\",\n  \"encrypted-traffic\" : {\n    \"enabled\" : false,\n    \"community-members\" : \"both center and satellite gateways\"\n  },\n  \"vpn-routing\" : \"to center only\",\n  \"mep\" : {\n    \"enabled\" : true,\n    \"entry-point-selection-mechanism\" : \"manual\",\n    \"entry-point-final-selection-mechanism\" : \"first to respond\",\n    \"tracking\" : \"user defined alert no.2\",\n    \"exception-priority-rules\" : [ {\n      \"satellite-gateways\" : [ {\n        \"uid\" : \"62a2e2cf-8372-4ac7-bd27-f268eae725ca\",\n        \"name\" : \"satGW3\",\n        \"type\" : \"simple-gateway\",\n        \"domain\" : {\n          \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n          \"name\" : \"SMC User\",\n          \"domain-type\" : \"domain\"\n        },\n        \"icon\" : \"NetworkObjects/gateway\",\n        \"color\" : \"black\"\n      } ],\n      \"first-priority-center-gateways\" : [ {\n        \"uid\" : \"cce61c09-6319-4219-a487-134fd0a4e45b\",\n        \"name\" : \"centerGW2\",\n        \"type\" : \"simple-gateway\",\n        \"domain\" : {\n          \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n          \"name\" : \"SMC User\",\n          \"domain-type\" : \"domain\"\n        },\n        \"icon\" : \"NetworkObjects/gateway\",\n        \"color\" : \"black\"\n      }, {\n        \"uid\" : \"184c53e4-6fed-450a-9e79-baac108703b2\",\n        \"name\" : \"centerGW1\",\n        \"type\" : \"simple-gateway\",\n        \"domain\" : {\n          \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n          \"name\" : \"SMC User\",\n          \"domain-type\" : \"domain\"\n        },\n        \"icon\" : \"NetworkObjects/gateway\",\n        \"color\" : \"black\"\n      } ],\n      \"second-priority-center-gateways\" : [ {\n        \"uid\" : \"72ad02ec-b735-435b-b02b-1c45bacdaa85\",\n        \"name\" : \"centerGW3\",\n        \"type\" : \"simple-gateway\",\n        \"domain\" : {\n          \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n          \"name\" : \"SMC User\",\n          \"domain-type\" : \"domain\"\n        },\n        \"icon\" : \"NetworkObjects/gateway\",\n        \"color\" : \"black\"\n      } ],\n      \"third-priority-center-gateways\" : [ {\n        \"uid\" : \"cfb98d59-713d-463b-8cbb-af463de8e293\",\n        \"name\" : \"centerGW4\",\n        \"type\" : \"simple-gateway\",\n        \"domain\" : {\n          \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n          \"name\" : \"SMC User\",\n          \"domain-type\" : \"domain\"\n        },\n        \"icon\" : \"NetworkObjects/gateway\",\n        \"color\" : \"black\"\n      } ]\n    } ],\n    \"default-priority-rule\" : {\n      \"first-priority-center-gateways\" : [ {\n        \"uid\" : \"97aeb369-9aea-11d5-bd16-0090272ccb30\",\n        \"name\" : \"Any\",\n        \"type\" : \"CpmiAnyObject\",\n        \"domain\" : {\n          \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n          \"name\" : \"Check Point Data\",\n          \"domain-type\" : \"data domain\"\n        },\n        \"icon\" : \"General/globalsAny\",\n        \"color\" : \"black\"\n      } ],\n      \"second-priority-center-gateways\" : [ {\n        \"uid\" : \"97aeb36a-9aea-11d5-bd16-0090272ccb30\",\n        \"name\" : \"None\",\n        \"type\" : \"CpmiAnyObject\",\n        \"domain\" : {\n          \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n          \"name\" : \"Check Point Data\",\n          \"domain-type\" : \"data domain\"\n        },\n        \"icon\" : \"General/globalsNone\",\n        \"color\" : \"black\"\n      } ],\n      \"third-priority-center-gateways\" : [ {\n        \"uid\" : \"97aeb36a-9aea-11d5-bd16-0090272ccb30\",\n        \"name\" : \"None\",\n        \"type\" : \"CpmiAnyObject\",\n        \"domain\" : {\n          \"uid\" : \"a0bbbc99-adef-4ef8-bb6d-defdefdefdef\",\n          \"name\" : \"Check Point Data\",\n          \"domain-type\" : \"data domain\"\n        },\n        \"icon\" : \"General/globalsNone\",\n        \"color\" : \"black\"\n      } ]\n    }\n  }\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:29.760976",
    "source_file": "show-vpn-community-star.html"
  }
}
```