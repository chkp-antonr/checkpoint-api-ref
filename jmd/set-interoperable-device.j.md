# set-interoperable-device

```json
{
  "command": "set-interoperable-device",
  "description": "Edit existing Interoperable Device.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/set-interoperable-device",
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
        "name": "ip-address",
        "description": "IPv4 or IPv6 address.",
        "type": "string",
        "required": false
      },
      {
        "name": "interfaces",
        "description": "",
        "type": "array",
        "required": false,
        "default": "prevent",
        "valid_values": [
          "prevent",
          "detect"
        ]
      },
      {
        "name": "add",
        "description": "",
        "type": "array",
        "required": false,
        "default": "prevent",
        "valid_values": [
          "prevent",
          "detect"
        ]
      },
      {
        "name": "name",
        "description": "Object name. Must be unique in the domain.",
        "type": "string",
        "required": true
      },
      {
        "name": "ip-address",
        "description": "IPv4 or IPv6 address. If both addresses are required use ipv4-address and ipv6-address fields explicitly.",
        "type": "string",
        "required": true
      },
      {
        "name": "network-mask",
        "description": "IPv4 or IPv6 network mask. If both masks are required use ipv4-network-mask and ipv6-network-mask fields explicitly. Instead of providing mask itself it is possible to specify IPv4 or IPv6 mask length in mask-length field. If both masks length are required use ipv4-mask-length and ipv6-mask-length fields explicitly.",
        "type": "string",
        "required": true
      },
      {
        "name": "anti-spoofing",
        "description": "Is anti spoofing enabled on the interface.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "anti-spoofing-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "prevent",
        "valid_values": [
          "prevent",
          "detect"
        ]
      },
      {
        "name": "action",
        "description": "If packets will be rejected (the Prevent option) or whether the packets will be monitored (the Detect option).",
        "type": "string",
        "required": false,
        "default": "prevent",
        "valid_values": [
          "prevent",
          "detect"
        ]
      },
      {
        "name": "exclude-packets",
        "description": "Don't check packets from excluded network.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "excluded-network-name",
        "description": "Excluded network name.",
        "type": "string",
        "required": false
      },
      {
        "name": "excluded-network-uid",
        "description": "Excluded network UID.",
        "type": "string",
        "required": false
      },
      {
        "name": "spoof-tracking",
        "description": "Spoof tracking.",
        "type": "string",
        "required": false,
        "default": "log",
        "valid_values": [
          "none",
          "log",
          "alert"
        ]
      },
      {
        "name": "topology",
        "description": "Topology configuration.",
        "type": "string",
        "required": false,
        "default": "internal",
        "valid_values": [
          "external",
          "internal"
        ]
      },
      {
        "name": "topology-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "not defined",
        "valid_values": [
          "not defined",
          "network defined by the interface ip and net mask",
          "network defined by routing",
          "specific"
        ]
      },
      {
        "name": "interface-leads-to-dmz",
        "description": "Whether this interface leads to demilitarized zone (perimeter network).",
        "type": "boolean",
        "required": false
      },
      {
        "name": "ip-address-behind-this-interface",
        "description": "Network settings behind this interface.",
        "type": "string",
        "required": false,
        "default": "not defined",
        "valid_values": [
          "not defined",
          "network defined by the interface ip and net mask",
          "network defined by routing",
          "specific"
        ]
      },
      {
        "name": "specific-network",
        "description": "Network behind this interface.",
        "type": "string",
        "required": false
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
        "name": "domains-to-process",
        "description": "Indicates which domains to process the commands on. It cannot be used with the details-level full, must be run from the System Domain only and with ignore-warnings true. Valid values are: CURRENT_DOMAIN, ALL_DOMAINS_ON_THIS_SERVER.",
        "type": "array",
        "required": false,
        "default": "CURRENT_DOMAIN"
      },
      {
        "name": "tags",
        "description": "Collection of tag identifiers.",
        "type": "Object",
        "required": false
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
        "description": "Object name. Must be unique in the domain.",
        "type": "string",
        "required": true
      },
      {
        "name": "ip-address",
        "description": "IPv4 or IPv6 address. If both addresses are required use ipv4-address and ipv6-address fields explicitly.",
        "type": "string",
        "required": true
      },
      {
        "name": "network-mask",
        "description": "IPv4 or IPv6 network mask. If both masks are required use ipv4-network-mask and ipv6-network-mask fields explicitly. Instead of providing mask itself it is possible to specify IPv4 or IPv6 mask length in mask-length field. If both masks length are required use ipv4-mask-length and ipv6-mask-length fields explicitly.",
        "type": "string",
        "required": true
      },
      {
        "name": "anti-spoofing",
        "description": "Is anti spoofing enabled on the interface.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "anti-spoofing-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "prevent",
        "valid_values": [
          "prevent",
          "detect"
        ]
      },
      {
        "name": "action",
        "description": "If packets will be rejected (the Prevent option) or whether the packets will be monitored (the Detect option).",
        "type": "string",
        "required": false,
        "default": "prevent",
        "valid_values": [
          "prevent",
          "detect"
        ]
      },
      {
        "name": "exclude-packets",
        "description": "Don't check packets from excluded network.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "excluded-network-name",
        "description": "Excluded network name.",
        "type": "string",
        "required": false
      },
      {
        "name": "excluded-network-uid",
        "description": "Excluded network UID.",
        "type": "string",
        "required": false
      },
      {
        "name": "spoof-tracking",
        "description": "Spoof tracking.",
        "type": "string",
        "required": false,
        "default": "log",
        "valid_values": [
          "none",
          "log",
          "alert"
        ]
      },
      {
        "name": "topology",
        "description": "Topology configuration.",
        "type": "string",
        "required": false,
        "default": "internal",
        "valid_values": [
          "external",
          "internal"
        ]
      },
      {
        "name": "topology-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "not defined",
        "valid_values": [
          "not defined",
          "network defined by the interface ip and net mask",
          "network defined by routing",
          "specific"
        ]
      },
      {
        "name": "interface-leads-to-dmz",
        "description": "Whether this interface leads to demilitarized zone (perimeter network).",
        "type": "boolean",
        "required": false
      },
      {
        "name": "ip-address-behind-this-interface",
        "description": "Network settings behind this interface.",
        "type": "string",
        "required": false,
        "default": "not defined",
        "valid_values": [
          "not defined",
          "network defined by the interface ip and net mask",
          "network defined by routing",
          "specific"
        ]
      },
      {
        "name": "specific-network",
        "description": "Network behind this interface.",
        "type": "string",
        "required": false
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
        "name": "domains-to-process",
        "description": "Indicates which domains to process the commands on. It cannot be used with the details-level full, must be run from the System Domain only and with ignore-warnings true. Valid values are: CURRENT_DOMAIN, ALL_DOMAINS_ON_THIS_SERVER.",
        "type": "array",
        "required": false,
        "default": "CURRENT_DOMAIN"
      },
      {
        "name": "tags",
        "description": "Collection of tag identifiers.",
        "type": "Object",
        "required": false
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
        "description": "Object name. Must be unique in the domain.",
        "type": "string",
        "required": true
      },
      {
        "name": "ip-address",
        "description": "IPv4 or IPv6 address. If both addresses are required use ipv4-address and ipv6-address fields explicitly.",
        "type": "string",
        "required": true
      },
      {
        "name": "network-mask",
        "description": "IPv4 or IPv6 network mask. If both masks are required use ipv4-network-mask and ipv6-network-mask fields explicitly. Instead of providing mask itself it is possible to specify IPv4 or IPv6 mask length in mask-length field. If both masks length are required use ipv4-mask-length and ipv6-mask-length fields explicitly.",
        "type": "string",
        "required": true
      },
      {
        "name": "anti-spoofing",
        "description": "Is anti spoofing enabled on the interface.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "anti-spoofing-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "prevent",
        "valid_values": [
          "prevent",
          "detect"
        ]
      },
      {
        "name": "action",
        "description": "If packets will be rejected (the Prevent option) or whether the packets will be monitored (the Detect option).",
        "type": "string",
        "required": false,
        "default": "prevent",
        "valid_values": [
          "prevent",
          "detect"
        ]
      },
      {
        "name": "exclude-packets",
        "description": "Don't check packets from excluded network.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "excluded-network-name",
        "description": "Excluded network name.",
        "type": "string",
        "required": false
      },
      {
        "name": "excluded-network-uid",
        "description": "Excluded network UID.",
        "type": "string",
        "required": false
      },
      {
        "name": "spoof-tracking",
        "description": "Spoof tracking.",
        "type": "string",
        "required": false,
        "default": "log",
        "valid_values": [
          "none",
          "log",
          "alert"
        ]
      },
      {
        "name": "topology",
        "description": "Topology configuration.",
        "type": "string",
        "required": false,
        "default": "internal",
        "valid_values": [
          "external",
          "internal"
        ]
      },
      {
        "name": "topology-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "not defined",
        "valid_values": [
          "not defined",
          "network defined by the interface ip and net mask",
          "network defined by routing",
          "specific"
        ]
      },
      {
        "name": "interface-leads-to-dmz",
        "description": "Whether this interface leads to demilitarized zone (perimeter network).",
        "type": "boolean",
        "required": false
      },
      {
        "name": "ip-address-behind-this-interface",
        "description": "Network settings behind this interface.",
        "type": "string",
        "required": false,
        "default": "not defined",
        "valid_values": [
          "not defined",
          "network defined by the interface ip and net mask",
          "network defined by routing",
          "specific"
        ]
      },
      {
        "name": "specific-network",
        "description": "Network behind this interface.",
        "type": "string",
        "required": false
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
        "name": "domains-to-process",
        "description": "Indicates which domains to process the commands on. It cannot be used with the details-level full, must be run from the System Domain only and with ignore-warnings true. Valid values are: CURRENT_DOMAIN, ALL_DOMAINS_ON_THIS_SERVER.",
        "type": "array",
        "required": false,
        "default": "CURRENT_DOMAIN"
      },
      {
        "name": "tags",
        "description": "Collection of tag identifiers.",
        "type": "Object",
        "required": false
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
        "description": "Object name. Must be unique in the domain.",
        "type": "string",
        "required": true
      },
      {
        "name": "ip-address",
        "description": "IPv4 or IPv6 address. If both addresses are required use ipv4-address and ipv6-address fields explicitly.",
        "type": "string",
        "required": true
      },
      {
        "name": "network-mask",
        "description": "IPv4 or IPv6 network mask. If both masks are required use ipv4-network-mask and ipv6-network-mask fields explicitly. Instead of providing mask itself it is possible to specify IPv4 or IPv6 mask length in mask-length field. If both masks length are required use ipv4-mask-length and ipv6-mask-length fields explicitly.",
        "type": "string",
        "required": true
      },
      {
        "name": "anti-spoofing",
        "description": "Is anti spoofing enabled on the interface.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "anti-spoofing-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "prevent",
        "valid_values": [
          "prevent",
          "detect"
        ]
      },
      {
        "name": "action",
        "description": "If packets will be rejected (the Prevent option) or whether the packets will be monitored (the Detect option).",
        "type": "string",
        "required": false,
        "default": "prevent",
        "valid_values": [
          "prevent",
          "detect"
        ]
      },
      {
        "name": "exclude-packets",
        "description": "Don't check packets from excluded network.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "excluded-network-name",
        "description": "Excluded network name.",
        "type": "string",
        "required": false
      },
      {
        "name": "excluded-network-uid",
        "description": "Excluded network UID.",
        "type": "string",
        "required": false
      },
      {
        "name": "spoof-tracking",
        "description": "Spoof tracking.",
        "type": "string",
        "required": false,
        "default": "log",
        "valid_values": [
          "none",
          "log",
          "alert"
        ]
      },
      {
        "name": "topology",
        "description": "Topology configuration.",
        "type": "string",
        "required": false,
        "default": "internal",
        "valid_values": [
          "external",
          "internal"
        ]
      },
      {
        "name": "topology-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "not defined",
        "valid_values": [
          "not defined",
          "network defined by the interface ip and net mask",
          "network defined by routing",
          "specific"
        ]
      },
      {
        "name": "interface-leads-to-dmz",
        "description": "Whether this interface leads to demilitarized zone (perimeter network).",
        "type": "boolean",
        "required": false
      },
      {
        "name": "ip-address-behind-this-interface",
        "description": "Network settings behind this interface.",
        "type": "string",
        "required": false,
        "default": "not defined",
        "valid_values": [
          "not defined",
          "network defined by the interface ip and net mask",
          "network defined by routing",
          "specific"
        ]
      },
      {
        "name": "specific-network",
        "description": "Network behind this interface.",
        "type": "string",
        "required": false
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
        "name": "domains-to-process",
        "description": "Indicates which domains to process the commands on. It cannot be used with the details-level full, must be run from the System Domain only and with ignore-warnings true. Valid values are: CURRENT_DOMAIN, ALL_DOMAINS_ON_THIS_SERVER.",
        "type": "array",
        "required": false,
        "default": "CURRENT_DOMAIN"
      },
      {
        "name": "tags",
        "description": "Collection of tag identifiers.",
        "type": "Object",
        "required": false
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
        "name": "vpn-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "addresses_behind_gw",
        "valid_values": [
          "manual",
          "addresses_behind_gw",
          "addresses_behind_nat"
        ]
      },
      {
        "name": "vpn-domain",
        "description": "Network group representing the customized encryption domain. Must be set when vpn-domain-type is set to 'manual' option.",
        "type": "string",
        "required": false
      },
      {
        "name": "vpn-domain-exclude-external-ip-addresses",
        "description": "Exclude the external IP addresses from the VPN domain of this Interoperable Device.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "vpn-domain-type",
        "description": "Indicates the encryption domain.",
        "type": "string",
        "required": false,
        "default": "addresses_behind_gw",
        "valid_values": [
          "manual",
          "addresses_behind_gw",
          "addresses_behind_nat"
        ]
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
        "name": "ipv4-address",
        "description": "IPv4 address of the Interoperable Device.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv6-address",
        "description": "IPv6 address of the Interoperable Device.",
        "type": "string",
        "required": false
      },
      {
        "name": "interfaces",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "prevent",
          "detect"
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
        "name": "ipv4-address",
        "description": "IPv4 address.",
        "type": "string",
        "required": false
      },
      {
        "name": "ipv4-mask-length",
        "description": "IPv4 network mask length.",
        "type": "integer",
        "required": false
      },
      {
        "name": "ipv4-network-mask",
        "description": "IPv4 network mask.",
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
        "name": "ipv6-mask-length",
        "description": "IPv6 network mask length.",
        "type": "integer",
        "required": false
      },
      {
        "name": "ipv6-network-mask",
        "description": "IPv6 network mask.",
        "type": "string",
        "required": false
      },
      {
        "name": "anti-spoofing",
        "description": "Is anti spoofing enabled on the interface.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "anti-spoofing-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "prevent",
          "detect"
        ]
      },
      {
        "name": "action",
        "description": "If packets will be rejected (the Prevent option) or whether the packets will be monitored (the Detect option).",
        "type": "string",
        "required": false,
        "valid_values": [
          "prevent",
          "detect"
        ]
      },
      {
        "name": "exclude-packets",
        "description": "Don't check packets from excluded network.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "excluded-network-name",
        "description": "Excluded network name.",
        "type": "string",
        "required": false
      },
      {
        "name": "excluded-network-uid",
        "description": "Excluded network UID.",
        "type": "string",
        "required": false
      },
      {
        "name": "spoof-tracking",
        "description": "Spoof tracking.",
        "type": "string",
        "required": false,
        "valid_values": [
          "none",
          "log",
          "alert"
        ]
      },
      {
        "name": "topology",
        "description": "Topology configuration.",
        "type": "string",
        "required": false,
        "valid_values": [
          "external",
          "internal"
        ]
      },
      {
        "name": "topology-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "not defined",
          "network defined by the interface ip and net mask",
          "network defined by routing",
          "specific"
        ]
      },
      {
        "name": "interface-leads-to-dmz",
        "description": "Whether this interface leads to demilitarized zone (perimeter network).",
        "type": "boolean",
        "required": false
      },
      {
        "name": "ip-address-behind-this-interface",
        "description": "Network settings behind this interface.",
        "type": "string",
        "required": false,
        "valid_values": [
          "not defined",
          "network defined by the interface ip and net mask",
          "network defined by routing",
          "specific"
        ]
      },
      {
        "name": "specific-network",
        "description": "Network behind this interface.",
        "type": "string",
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
        "name": "vpn-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "manual",
          "addresses_behind_gw",
          "addresses_behind_nat"
        ]
      },
      {
        "name": "vpn-domain",
        "description": "Network group representing the customized encryption domain. Must be set when vpn-domain-type is set to 'manual' option.",
        "type": "Object",
        "required": false
      },
      {
        "name": "vpn-domain-exclude-external-ip-addresses",
        "description": "Exclude the external IP addresses from the VPN domain of this Interoperable Device.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "vpn-domain-type",
        "description": "Indicates the encryption domain.",
        "type": "string",
        "required": false,
        "valid_values": [
          "manual",
          "addresses_behind_gw",
          "addresses_behind_nat"
        ]
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
        "name": "tags",
        "description": "Collection of tag objects identified by the name or UID.",
        "type": "array",
        "required": false
      },
      {
        "name": "type",
        "description": "Object type.",
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
    "set-interoperable-device": {
      "description": "Sets simple Interoperable Device",
      "request": "POST {{server}}/set-interoperable-device\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"NewInteroperableDevice\",\n  \"ip-address\" : \"192.168.1.6\"\n}",
      "response": "{\n  \"uid\" : \"f4513b7d-dbec-4a00-9e6e-c9ece47d8ca8\",\n  \"name\" : \"NewInteroperableDevice\",\n  \"type\" : \"interop\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1630493931275,\n      \"iso-8601\" : \"2021-09-01T13:58+0300\"\n    },\n    \"last-modifier\" : \"WEB_API\",\n    \"creation-time\" : {\n      \"posix\" : 1630493694250,\n      \"iso-8601\" : \"2021-09-01T13:54+0300\"\n    },\n    \"creator\" : \"WEB_API\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : true,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"NetworkObjects/gateway\",\n  \"groups\" : [ ],\n  \"ipv4-address\" : \"192.168.1.6\",\n  \"ipv6-address\" : \"\",\n  \"vpn-settings\" : {\n    \"vpn-domain-type\" : \"addresses_behind_gw\"\n  },\n  \"interfaces\" : [ ]\n}"
    },
    "set-interoperable-device with a new added interface to the existing interfaces": {
      "description": "Sets Interoperable Device with a new added interface to the existing interfaces",
      "request": "POST {{server}}/set-interoperable-device\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"NewInteroperableDevice\",\n  \"interfaces.add.ip-address\" : \"100.170.200.0\",\n  \"interfaces.add.network-mask\" : \"255.255.255.0\",\n  \"interfaces.add.name\" : \"externalInterface\",\n  \"interfaces.add.topology\" : \"external\"\n}",
      "response": "{\n  \"uid\" : \"fa094741-761e-4c44-931e-e31cd80e6dca\",\n  \"name\" : \"NewInteroperableDevice\",\n  \"type\" : \"interoperable-device\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1633250949337,\n      \"iso-8601\" : \"2021-10-03T11:49+0300\"\n    },\n    \"last-modifier\" : \"aa\",\n    \"creation-time\" : {\n      \"posix\" : 1633250945244,\n      \"iso-8601\" : \"2021-10-03T11:49+0300\"\n    },\n    \"creator\" : \"aa\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : true,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"NetworkObjects/gateway\",\n  \"groups\" : [ ],\n  \"ipv4-address\" : \"192.168.10.1\",\n  \"vpn-settings\" : {\n    \"vpn-domain-type\" : \"addresses_behind_gw\"\n  },\n  \"interfaces\" : [ {\n    \"uid\" : \"93d247f5-8c63-46b7-a863-5bc6e3218eba\",\n    \"name\" : \"internalInterface\",\n    \"type\" : \"CpmiInterface\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"tags\" : [ ],\n    \"comments\" : \"\",\n    \"color\" : \"black\",\n    \"icon\" : \"Unknown\",\n    \"ipv4-address\" : \"100.150.200.0\",\n    \"ipv4-network-mask\" : \"255.255.255.0\",\n    \"ipv4-mask-length\" : 24,\n    \"topology\" : \"internal\",\n    \"topology-settings\" : {\n      \"ip-address-behind-this-interface\" : \"not defined\",\n      \"interface-leads-to-dmz\" : false\n    },\n    \"anti-spoofing\" : false\n  }, {\n    \"uid\" : \"6af47671-3f5d-4440-a27f-576236b942eb\",\n    \"name\" : \"externalInterface\",\n    \"type\" : \"CpmiInterface\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"tags\" : [ ],\n    \"comments\" : \"\",\n    \"icon\" : \"Unknown\",\n    \"ipv4-address\" : \"100.170.200.0\",\n    \"ipv4-network-mask\" : \"255.255.255.0\",\n    \"ipv4-mask-length\" : 24,\n    \"topology\" : \"external\",\n    \"anti-spoofing\" : true,\n    \"anti-spoofing-settings\" : {\n      \"action\" : \"prevent\",\n      \"exclude-packets\" : false,\n      \"spoof-tracking\" : \"log\"\n    }\n  } ]\n}"
    },
    "set-interoperable-device with a different IPv4 address": {
      "description": "Sets Interoperable Device with a different IPv4 address",
      "request": "POST {{server}}/set-interoperable-device\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"NewInteroperableDevice\",\n  \"ipv4-address\" : \"192.168.1.6\"\n}",
      "response": "{\n  \"uid\" : \"f4513b7d-dbec-4a00-9e6e-c9ece47d8ca8\",\n  \"name\" : \"NewInteroperableDevice\",\n  \"type\" : \"interop\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1630493719955,\n      \"iso-8601\" : \"2021-09-01T13:55+0300\"\n    },\n    \"last-modifier\" : \"WEB_API\",\n    \"creation-time\" : {\n      \"posix\" : 1630493694250,\n      \"iso-8601\" : \"2021-09-01T13:54+0300\"\n    },\n    \"creator\" : \"WEB_API\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : true,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"NetworkObjects/gateway\",\n  \"groups\" : [ ],\n  \"ipv4-address\" : \"192.168.1.6\",\n  \"ipv6-address\" : \"\",\n  \"vpn-settings\" : {\n    \"vpn-domain-type\" : \"addresses_behind_gw\"\n  },\n  \"interfaces\" : [ ]\n}"
    },
    "set-interoperable-device with a different IPv4 and IPv6 addresses": {
      "description": "Sets Interoperable Device with a different IPv4 and IPv6 addresses",
      "request": "POST {{server}}/set-interoperable-device\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"NewInteroperableDevice\",\n  \"ipv4-address\" : \"192.168.1.6\",\n  \"ipv6-address\" : \"2001:0db8:85a3:0000:0000:8a2e:0370:7334\"\n}",
      "response": "{\n  \"uid\" : \"4fa631c7-46f5-479a-9b81-d39277056e50\",\n  \"name\" : \"NewInteroperableDevice\",\n  \"type\" : \"interop\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1630497132990,\n      \"iso-8601\" : \"2021-09-01T14:52+0300\"\n    },\n    \"last-modifier\" : \"WEB_API\",\n    \"creation-time\" : {\n      \"posix\" : 1630495698947,\n      \"iso-8601\" : \"2021-09-01T14:28+0300\"\n    },\n    \"creator\" : \"WEB_API\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : true,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"NetworkObjects/gateway\",\n  \"groups\" : [ ],\n  \"ipv4-address\" : \"192.168.1.6\",\n  \"ipv6-address\" : \"2001:db8:85a3::8a2e:370:7334\",\n  \"vpn-settings\" : {\n    \"vpn-domain-type\" : \"addresses_behind_gw\"\n  },\n  \"interfaces\" : [ ]\n}"
    },
    "set-interoperable-device with a different IPv6 address": {
      "description": "Sets Interoperable Device with a different IPv6 address",
      "request": "POST {{server}}/add-interoperable-device\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"NewInteroperableDevice\",\n  \"ipv6-address\" : \"2001:0db8:85a3:0000:0000:8a2e:0370:7334\"\n}",
      "response": "{\n  \"uid\" : \"4fa631c7-46f5-479a-9b81-d39277056e50\",\n  \"name\" : \"NewInteroperableDevice\",\n  \"type\" : \"interop\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1630497367736,\n      \"iso-8601\" : \"2021-09-01T14:56+0300\"\n    },\n    \"last-modifier\" : \"WEB_API\",\n    \"creation-time\" : {\n      \"posix\" : 1630495698947,\n      \"iso-8601\" : \"2021-09-01T14:28+0300\"\n    },\n    \"creator\" : \"WEB_API\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : true,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"NetworkObjects/gateway\",\n  \"groups\" : [ ],\n  \"ipv4-address\" : \"192.168.1.6\",\n  \"ipv6-address\" : \"2001:db8:85a3::8a2e:370:7334\",\n  \"vpn-settings\" : {\n    \"vpn-domain-type\" : \"addresses_behind_gw\"\n  },\n  \"interfaces\" : [ ]\n}"
    },
    "set-interoperable-device with removing existing interface": {
      "description": "Sets Interoperable Device with removing existing interface",
      "request": "POST {{server}}/set-interoperable-device\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"NewInteroperableDevice\",\n  \"interfaces.remove\" : \"externalInterface\"\n}",
      "response": "{\n  \"uid\" : \"405d329c-cac6-4002-b7ce-b15800c78fcc\",\n  \"name\" : \"NewInteroperableDevice\",\n  \"type\" : \"interoperable-device\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1633253999980,\n      \"iso-8601\" : \"2021-10-03T12:39+0300\"\n    },\n    \"last-modifier\" : \"WEB_API\",\n    \"creation-time\" : {\n      \"posix\" : 1633250910424,\n      \"iso-8601\" : \"2021-10-03T11:48+0300\"\n    },\n    \"creator\" : \"WEB_API\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : true,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"NetworkObjects/gateway\",\n  \"groups\" : [ ],\n  \"ipv4-address\" : \"192.168.10.5\",\n  \"vpn-settings\" : {\n    \"vpn-domain-type\" : \"addresses_behind_gw\"\n  },\n  \"interfaces\" : [ ]\n}"
    },
    "set-interoperable-device with a new set of interface": {
      "description": "Sets Interoperable Device with a new set of interface",
      "request": "POST {{server}}/set-interoperable-device\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"NewInteroperableDevice\",\n  \"interfaces.ip-address\" : \"192.168.10.8\",\n  \"interfaces.mask-length\" : \"24\",\n  \"interfaces.name\" : \"internalInterface\"\n}",
      "response": "{\n  \"uid\" : \"4a51636d-e4e3-44d8-9ef8-f592b2f387f7\",\n  \"name\" : \"NewInteroperableDevice\",\n  \"type\" : \"interoperable-device\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1633250949621,\n      \"iso-8601\" : \"2021-10-03T11:49+0300\"\n    },\n    \"last-modifier\" : \"aa\",\n    \"creation-time\" : {\n      \"posix\" : 1633250945655,\n      \"iso-8601\" : \"2021-10-03T11:49+0300\"\n    },\n    \"creator\" : \"aa\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : true,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"NetworkObjects/gateway\",\n  \"groups\" : [ ],\n  \"ipv4-address\" : \"192.168.10.3\",\n  \"vpn-settings\" : {\n    \"vpn-domain-type\" : \"addresses_behind_gw\"\n  },\n  \"interfaces\" : [ {\n    \"uid\" : \"5185f9ad-60e8-4812-b62a-616e0d1d97f7\",\n    \"name\" : \"internalInterface\",\n    \"type\" : \"CpmiInterface\",\n    \"domain\" : {\n      \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n      \"name\" : \"SMC User\",\n      \"domain-type\" : \"domain\"\n    },\n    \"tags\" : [ ],\n    \"comments\" : \"\",\n    \"icon\" : \"Unknown\",\n    \"ipv4-address\" : \"192.168.10.8\",\n    \"topology\" : \"internal\",\n    \"topology-settings\" : {\n      \"ip-address-behind-this-interface\" : \"not defined\",\n      \"interface-leads-to-dmz\" : false\n    },\n    \"anti-spoofing\" : false\n  } ]\n}"
    },
    "set-interoperable-device with a different vpn-domain": {
      "description": "Sets Interoperable Device with a different vpn-domain option",
      "request": "POST {{server}}/add-interoperable-device\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"name\" : \"NewInteroperableDevice\",\n  \"vpn-settings.vpn-domain-type\" : \"manual\",\n  \"vpn-settings.vpn-domain\" : \"InteroperableDevice_Network_2\"\n}",
      "response": "{\n  \"uid\" : \"4fa631c7-46f5-479a-9b81-d39277056e50\",\n  \"name\" : \"NewInteroperableDevice\",\n  \"type\" : \"interop\",\n  \"domain\" : {\n    \"uid\" : \"41e821a0-3720-11e3-aa6e-0800200c9fde\",\n    \"name\" : \"SMC User\",\n    \"domain-type\" : \"domain\"\n  },\n  \"meta-info\" : {\n    \"lock\" : \"unlocked\",\n    \"validation-state\" : \"ok\",\n    \"last-modify-time\" : {\n      \"posix\" : 1630497573291,\n      \"iso-8601\" : \"2021-09-01T14:59+0300\"\n    },\n    \"last-modifier\" : \"WEB_API\",\n    \"creation-time\" : {\n      \"posix\" : 1630495698947,\n      \"iso-8601\" : \"2021-09-01T14:28+0300\"\n    },\n    \"creator\" : \"WEB_API\"\n  },\n  \"tags\" : [ ],\n  \"read-only\" : true,\n  \"comments\" : \"\",\n  \"color\" : \"black\",\n  \"icon\" : \"NetworkObjects/gateway\",\n  \"groups\" : [ ],\n  \"ipv4-address\" : \"192.168.1.6\",\n  \"ipv6-address\" : \"2001:db8:85a3::8a2e:370:7334\",\n  \"vpn-settings\" : {\n    \"vpn-domain-type\" : \"manual\",\n    \"vpn-domain\" : \"InteroperableDevice_Network_2\"\n  },\n  \"interfaces\" : [ ]\n}"
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:17.784758",
    "source_file": "set-interoperable-device.html"
  }
}
```