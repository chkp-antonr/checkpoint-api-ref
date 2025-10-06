# set-global-properties

```json
{
  "command": "set-global-properties",
  "description": "Edit Global Properties.",
  "request": {
    "url": "POST https://<mgmt-server>:<port>/web_api/set-global-properties",
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
        "name": "firewall",
        "description": "",
        "type": "array",
        "required": false,
        "default": "true",
        "valid_values": [
          "first",
          "last",
          "before last"
        ]
      },
      {
        "name": "accept-control-connections",
        "description": "Used for: Installing the security policy from the Security Management server to the gateways. Sending logs from the gateways to the Security Management server. Communication between SmartConsole clients and the Security Management Server Communication between Firewall daemons on different machines (Security Management Server, Security Gateway). Connecting to OPSEC applications such as RADIUS and TACACS authentication servers.If you disable Accept Control Connections and you want Check Point components to communicate with each other and with OPSEC components, you must explicitly allow these connections in the Rule Base.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "accept-ips1-management-connections",
        "description": "Accepts IPS-1 connections.Available only if accept-control-connections is true.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "accept-remote-access-control-connections",
        "description": "Accepts Remote Access connections.Available only if accept-control-connections is true.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "accept-smart-update-connections",
        "description": "Accepts SmartUpdate connections.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "accept-outgoing-packets-originating-from-gw",
        "description": "Accepts all packets from connections that originate at the Check Point Security Gateway.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "accept-outgoing-packets-originating-from-gw-position",
        "description": "The position of the implied rules in the Rule Base.Available only if accept-outgoing-packets-originating-from-gw is false.",
        "type": "string",
        "required": false,
        "default": "before last",
        "valid_values": [
          "first",
          "last",
          "before last"
        ]
      },
      {
        "name": "accept-outgoing-packets-originating-from-connectra-gw",
        "description": "Accepts outgoing packets originating from Connectra gateway.Available only if accept-outgoing-packets-originating-from-gw is false.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "accept-outgoing-packets-to-cp-online-services",
        "description": "Allow Security Gateways to access Check Point online services. Supported for R80.10 Gateway and higher.Available only if accept-outgoing-packets-originating-from-gw is false.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "accept-outgoing-packets-to-cp-online-services-position",
        "description": "The position of the implied rules in the Rule Base.Available only if accept-outgoing-packets-to-cp-online-services is true.",
        "type": "string",
        "required": false,
        "default": "before last",
        "valid_values": [
          "first",
          "last",
          "before last"
        ]
      },
      {
        "name": "accept-domain-name-over-tcp",
        "description": "Accepts Domain Name (DNS) queries and replies over TCP, to allow downloading of the domain name-resolving tables used for zone transfers between servers. For clients, DNS over TCP is only used if the tables to be transferred are very large.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "accept-domain-name-over-tcp-position",
        "description": "The position of the implied rules in the Rule Base.Available only if accept-domain-name-over-tcp is true.",
        "type": "string",
        "required": false,
        "default": "first",
        "valid_values": [
          "first",
          "last",
          "before last"
        ]
      },
      {
        "name": "accept-domain-name-over-udp",
        "description": "Accepts Domain Name (DNS) queries and replies over UDP.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "accept-domain-name-over-udp-position",
        "description": "The position of the implied rules in the Rule Base.Available only if accept-domain-name-over-udp is true.",
        "type": "string",
        "required": false,
        "default": "first",
        "valid_values": [
          "first",
          "last",
          "before last"
        ]
      },
      {
        "name": "accept-dynamic-addr-modules-outgoing-internet-connections",
        "description": "Accept Dynamic Address modules' outgoing internet connections.Accepts DHCP traffic for DAIP (Dynamically Assigned IP Address) gateways. In Small Office Appliance gateways, this rule allows outgoing DHCP, PPP, PPTP and L2TP Internet connections (regardless of whether it is or is not a DAIP gateway).",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "accept-icmp-requests",
        "description": "Accepts Internet Control Message Protocol messages.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "accept-icmp-requests-position",
        "description": "The position of the implied rules in the Rule Base.Available only if accept-icmp-requests is true.",
        "type": "string",
        "required": false,
        "default": "before last",
        "valid_values": [
          "first",
          "last",
          "before last"
        ]
      },
      {
        "name": "accept-identity-awareness-control-connections",
        "description": "Accepts traffic between Security Gateways in distributed environment configurations of Identity Awareness.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "accept-identity-awareness-control-connections-position",
        "description": "The position of the implied rules in the Rule Base.Available only if accept-identity-awareness-control-connections is true.",
        "type": "string",
        "required": false,
        "default": "first",
        "valid_values": [
          "first",
          "last",
          "before last"
        ]
      },
      {
        "name": "accept-incoming-traffic-to-dhcp-and-dns-services-of-gws",
        "description": "Allows the Small Office Appliance gateway to provide DHCP relay, DHCP server and DNS proxy services regardless of the rule base.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "accept-rip",
        "description": "Accepts Routing Information Protocol (RIP), using UDP on port 520.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "accept-rip-position",
        "description": "The position of the implied rules in the Rule Base.Available only if accept-rip is true.",
        "type": "string",
        "required": false,
        "default": "first",
        "valid_values": [
          "first",
          "last",
          "before last"
        ]
      },
      {
        "name": "accept-vrrp-packets-originating-from-cluster-members",
        "description": "Selecting this option creates an implied rule in the security policy Rule Base that accepts VRRP inbound and outbound traffic to and from the members of the cluster.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "accept-web-and-ssh-connections-for-gw-administration",
        "description": "Accepts Web and SSH connections for Small Office Appliance gateways.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "log-implied-rules",
        "description": "Produces log records for communications that match the implied rules that are generated in the Rule Base from the properties defined in this window.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "security-server",
        "description": "",
        "type": "array",
        "required": false,
        "default": "80",
        "valid_values": [
          "standard",
          "post request",
          "every request"
        ]
      },
      {
        "name": "client-auth-welcome-file",
        "description": "Client authentication welcome file is the name of a file whose contents are to be displayed when a user begins a Client Authenticated session (optional) using the Manual Sign On Method. Client Authenticated Sessions initiated by Manual Sign On are not mediated by a security server.",
        "type": "string",
        "required": false
      },
      {
        "name": "ftp-welcome-msg-file",
        "description": "FTP welcome message file is the name of a file whose contents are to be displayed when a user begins an Authenticated FTP session.",
        "type": "string",
        "required": false
      },
      {
        "name": "rlogin-welcome-msg-file",
        "description": "Rlogin welcome message file is the name of a file whose contents are to be displayed when a user begins an Authenticated RLOGIN session.",
        "type": "string",
        "required": false
      },
      {
        "name": "telnet-welcome-msg-file",
        "description": "Telnet welcome message file is the name of a file whose contents are to be displayed when a user begins an Authenticated Telnet session.",
        "type": "string",
        "required": false
      },
      {
        "name": "mdq-welcome-msg",
        "description": "MDQ Welcome Message is the message to be displayed when a user begins an MDQ session. The MDQ Welcome Message should contain characters according to RFC 1035 and it must follow the ARPANET host name rules: - This message must begin with a number or letter. After the first letter or number character the remaining characters can be a letter, number, space, tab or hyphen. - This message must not end with a space or a tab and is limited to 63 characters.",
        "type": "string",
        "required": false
      },
      {
        "name": "smtp-welcome-msg",
        "description": "SMTP Welcome Message is the message to be displayed when a user begins an SMTP session.",
        "type": "string",
        "required": false
      },
      {
        "name": "http-servers",
        "description": "",
        "type": "array",
        "required": false,
        "default": "80",
        "valid_values": [
          "standard",
          "post request",
          "every request"
        ]
      },
      {
        "name": "add",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "80",
        "valid_values": [
          "standard",
          "post request",
          "every request"
        ]
      },
      {
        "name": "logical-name",
        "description": "Unique Logical Name of the HTTP Server.",
        "type": "string",
        "required": true
      },
      {
        "name": "host",
        "description": "Host name of the HTTP Server.",
        "type": "string",
        "required": true
      },
      {
        "name": "port",
        "description": "Port number of the HTTP Server.",
        "type": "integer",
        "required": false,
        "default": "80"
      },
      {
        "name": "reauthentication",
        "description": "Specify whether users must reauthenticate when accessing a specific server.",
        "type": "string",
        "required": false,
        "default": "Standard",
        "valid_values": [
          "standard",
          "post request",
          "every request"
        ]
      },
      {
        "name": "logical-name",
        "description": "Unique Logical Name of the HTTP Server.",
        "type": "string",
        "required": true
      },
      {
        "name": "host",
        "description": "Host name of the HTTP Server.",
        "type": "string",
        "required": true
      },
      {
        "name": "port",
        "description": "Port number of the HTTP Server.",
        "type": "integer",
        "required": false,
        "default": "80"
      },
      {
        "name": "reauthentication",
        "description": "Specify whether users must reauthenticate when accessing a specific server.",
        "type": "string",
        "required": false,
        "default": "Standard",
        "valid_values": [
          "standard",
          "post request",
          "every request"
        ]
      },
      {
        "name": "remove",
        "description": "Removes from collection of values",
        "type": "string",
        "required": false
      },
      {
        "name": "logical-name",
        "description": "Unique Logical Name of the HTTP Server.",
        "type": "string",
        "required": true
      },
      {
        "name": "host",
        "description": "Host name of the HTTP Server.",
        "type": "string",
        "required": true
      },
      {
        "name": "port",
        "description": "Port number of the HTTP Server.",
        "type": "integer",
        "required": false,
        "default": "80"
      },
      {
        "name": "reauthentication",
        "description": "Specify whether users must reauthenticate when accessing a specific server.",
        "type": "string",
        "required": false,
        "default": "Standard",
        "valid_values": [
          "standard",
          "post request",
          "every request"
        ]
      },
      {
        "name": "logical-name",
        "description": "Unique Logical Name of the HTTP Server.",
        "type": "string",
        "required": true
      },
      {
        "name": "host",
        "description": "Host name of the HTTP Server.",
        "type": "string",
        "required": true
      },
      {
        "name": "port",
        "description": "Port number of the HTTP Server.",
        "type": "integer",
        "required": false,
        "default": "80"
      },
      {
        "name": "reauthentication",
        "description": "Specify whether users must reauthenticate when accessing a specific server.",
        "type": "string",
        "required": false,
        "default": "Standard",
        "valid_values": [
          "standard",
          "post request",
          "every request"
        ]
      },
      {
        "name": "server-for-null-requests",
        "description": "The Logical Name of a Null Requests Server from http-servers.",
        "type": "string",
        "required": false
      },
      {
        "name": "nat",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "true",
        "valid_values": [
          "ip allocation log",
          "none"
        ]
      },
      {
        "name": "allow-bi-directional-nat",
        "description": "Applies to automatic NAT rules in the NAT Rule Base, and allows two automatic NAT rules to match a connection. Without Bidirectional NAT, only one automatic NAT rule can match a connection.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "auto-arp-conf",
        "description": "Ensures that ARP requests for a translated (NATed) machine, network or address range are answered by the Check Point Security Gateway.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "merge-manual-proxy-arp-conf",
        "description": "Merges the automatic and manual ARP configurations. Manual proxy ARP configuration is required for manual Static NAT rules.Available only if auto-arp-conf is true.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "auto-translate-dest-on-client-side",
        "description": "Applies to packets originating at the client, with the server as its destination. Static NAT for the server is performed on the client side.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "manually-translate-dest-on-client-side",
        "description": "Applies to packets originating at the client, with the server as its destination. Static NAT for the server is performed on the client side.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "enable-ip-pool-nat",
        "description": "Applies to packets originating at the client, with the server as its destination. Static NAT for the server is performed on the client side.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "addr-alloc-and-release-track",
        "description": "Specifies whether to log each allocation and release of an IP address from the IP Pool.Available only if enable-ip-pool-nat is true.",
        "type": "string",
        "required": false,
        "valid_values": [
          "ip allocation log",
          "none"
        ]
      },
      {
        "name": "addr-exhaustion-track",
        "description": "Specifies the action to take if the IP Pool is exhausted.Available only if enable-ip-pool-nat is true.",
        "type": "string",
        "required": false,
        "valid_values": [
          "ip exhaustion alert",
          "none",
          "ip exhaustion log"
        ]
      },
      {
        "name": "authentication",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "true"
      },
      {
        "name": "auth-internal-users-with-specific-suffix",
        "description": "Enforce suffix for internal users authentication.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "allowed-suffix-for-internal-users",
        "description": "Suffix for internal users authentication.",
        "type": "string",
        "required": false
      },
      {
        "name": "max-days-before-expiration-of-non-pulled-user-certificates",
        "description": "Users certificates which were initiated but not pulled will expire after the specified number of days. Any value from 1 to 60 days can be entered in this field.",
        "type": "integer",
        "required": false,
        "default": "14"
      },
      {
        "name": "max-client-auth-attempts-before-connection-termination",
        "description": "Allowed Number of Failed Client Authentication Attempts Before Session Termination. Any value from 1 to 800 attempts can be entered in this field.",
        "type": "integer",
        "required": false,
        "default": "3"
      },
      {
        "name": "max-rlogin-attempts-before-connection-termination",
        "description": "Allowed Number of Failed rlogin Attempts Before Session Termination. Any value from 1 to 800 attempts can be entered in this field.",
        "type": "integer",
        "required": false,
        "default": "3"
      },
      {
        "name": "max-session-auth-attempts-before-connection-termination",
        "description": "Allowed Number of Failed Session Authentication Attempts Before Session Termination. Any value from 1 to 800 attempts can be entered in this field.",
        "type": "integer",
        "required": false,
        "default": "3"
      },
      {
        "name": "max-telnet-attempts-before-connection-termination",
        "description": "Allowed Number of Failed telnet Attempts Before Session Termination. Any value from 1 to 800 attempts can be entered in this field.",
        "type": "integer",
        "required": false,
        "default": "3"
      },
      {
        "name": "enable-delayed-auth",
        "description": "all authentications other than certificate-based authentications will be delayed by the specified time. Applying this delay will stall brute force authentication attacks. The delay is applied for both failed and successful authentication attempts.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "delay-each-auth-attempt-by",
        "description": "Delay each authentication attempt by the specified number of milliseconds. Any value from 1 to 25000 can be entered in this field.",
        "type": "integer",
        "required": false,
        "default": "100"
      },
      {
        "name": "vpn",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "simplified",
        "valid_values": [
          "simplified",
          "traditional",
          "per policy"
        ]
      },
      {
        "name": "vpn-conf-method",
        "description": "Decide on Simplified or Traditional mode for all new security policies or decide which mode to use on a policy by policy basis.",
        "type": "string",
        "required": false,
        "default": "simplified",
        "valid_values": [
          "simplified",
          "traditional",
          "per policy"
        ]
      },
      {
        "name": "domain-name-for-dns-resolving",
        "description": "Enter the domain name that will be used for gateways DNS lookup. The DNS host name that is used is \"gateway_name.domain_name\".",
        "type": "string",
        "required": false
      },
      {
        "name": "enable-backup-gw",
        "description": "Enable Backup Gateway.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "enable-decrypt-on-accept-for-gw-to-gw-traffic",
        "description": "Enable decrypt on accept for gateway to gateway traffic. This is only relevant for policies in traditional mode. In Traditional Mode, the 'Accept' action determines that a connection is allowed, while the 'Encrypt' action determines that a connection is allowed and encrypted. Select whether VPN accepts an encrypted packet that matches a rule with an 'Accept' action or drops it.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "enable-load-distribution-for-mep-conf",
        "description": "Enable load distribution for Multiple Entry Points configurations (Site To Site connections). The VPN Multiple Entry Point (MEP) feature supplies high availability and load distribution for Check Point Security Gateways. MEP works in four modes: First to Respond, in which the first gateway to reply to the peer gateway is chosen. An organization would choose this option if, for example, the organization has two gateways in a MEPed configuration - one in London, the other in New York. It makes sense for Check Point Security Gateway peers located in England to try the London gateway first and the NY gateway second. Being geographically closer to Check Point Security Gateway peers in England, the London gateway will be the first to respond, and becomes the entry point to the internal network. VPN Domain, is when the destination IP belongs to a particular VPN domain, the gateway of that domain becomes the chosen entry point. This gateway becomes the primary gateway while other gateways in the MEP configuration become its backup gateways. Random Selection, in which the remote Check Point Security Gateway peer randomly selects a gateway with which to open a VPN connection. For each IP source/destination address pair, a new gateway is randomly selected. An organization might have a number of machines with equal performance abilities. In this case, it makes sense to enable load distribution. The machines are used in a random and equal way. Manually set priority list, gateway priorities can be set manually for the entire community or for individual satellite gateways..",
        "type": "boolean",
        "required": false
      },
      {
        "name": "enable-vpn-directional-match-in-vpn-column",
        "description": "Enable VPN Directional Match in VPN Column.Note: VPN Directional Match is supported only on Gaia, SecurePlatform, Linux and IPSO.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "grace-period-after-the-crl-is-not-valid",
        "description": "When establishing VPN tunnels, the peer presents its certificate for authentication. The clock on the gateway machine must be synchronized with the clock on the Certificate Authority machine. Otherwise, the Certificate Revocation List (CRL) used for validating the peer's certificate may be considered invalid and thus the authentication fails. To resolve the issue of differing clock times, a Grace Period permits a wider window for CRL validity.",
        "type": "integer",
        "required": false,
        "default": "1800"
      },
      {
        "name": "grace-period-before-the-crl-is-valid",
        "description": "When establishing VPN tunnels, the peer presents its certificate for authentication. The clock on the gateway machine must be synchronized with the clock on the Certificate Authority machine. Otherwise, the Certificate Revocation List (CRL) used for validating the peer's certificate may be considered invalid and thus the authentication fails. To resolve the issue of differing clock times, a Grace Period permits a wider window for CRL validity.",
        "type": "integer",
        "required": false,
        "default": "7200"
      },
      {
        "name": "grace-period-extension-for-secure-remote-secure-client",
        "description": "When dealing with remote clients the Grace Period needs to be extended. The remote client sometimes relies on the peer gateway to supply the CRL. If the client's clock is not synchronized with the gateway's clock, a CRL that is considered valid by the gateway may be considered invalid by the client.",
        "type": "integer",
        "required": false,
        "default": "3600"
      },
      {
        "name": "support-ike-dos-protection-from-identified-src",
        "description": "When the number of IKE negotiations handled simultaneously exceeds a threshold above VPN's capacity, a gateway concludes that it is either under a high load or experiencing a Denial of Service attack. VPN can filter out peers that are the probable source of the potential Denial of Service attack. There are two kinds of protection: Stateless - the peer has to respond to an IKE notification in a way that proves the peer's IP address is not spoofed. If the peer cannot prove this, VPN does not allocate resources for the IKE negotiation Puzzles - this is the same as Stateless, but in addition, the peer has to solve a mathematical puzzle. Solving this puzzle consumes peer CPU resources in a way that makes it difficult to initiate multiple IKE negotiations simultaneously.Puzzles is more secure then Stateless, but affects performance.Since these kinds of attacks involve a new proprietary addition to the IKE protocol, enabling these protection mechanisms may cause difficulties with non Check Point VPN products or older versions of VPN.",
        "type": "string",
        "required": false,
        "default": "stateless",
        "valid_values": [
          "puzzles",
          "stateless",
          "none"
        ]
      },
      {
        "name": "support-ike-dos-protection-from-unidentified-src",
        "description": "When the number of IKE negotiations handled simultaneously exceeds a threshold above VPN's capacity, a gateway concludes that it is either under a high load or experiencing a Denial of Service attack. VPN can filter out peers that are the probable source of the potential Denial of Service attack. There are two kinds of protection: Stateless - the peer has to respond to an IKE notification in a way that proves the peer's IP address is not spoofed. If the peer cannot prove this, VPN does not allocate resources for the IKE negotiation Puzzles - this is the same as Stateless, but in addition, the peer has to solve a mathematical puzzle. Solving this puzzle consumes peer CPU resources in a way that makes it difficult to initiate multiple IKE negotiations simultaneously.Puzzles is more secure then Stateless, but affects performance.Since these kinds of attacks involve a new proprietary addition to the IKE protocol, enabling these protection mechanisms may cause difficulties with non Check Point VPN products or older versions of VPN.",
        "type": "string",
        "required": false,
        "default": "puzzles",
        "valid_values": [
          "puzzles",
          "stateless",
          "none"
        ]
      },
      {
        "name": "identity-awareness",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "1-2880"
        ]
      },
      {
        "name": "cache-mode",
        "description": "True: In case of connectivity loss from the Policy-Decision-Point (PDP), extend Identity cache up-to \"cache-mode-duration\".False: Identity Cache Mode is disabled, in case of connectivity loss from the Policy-Decision-Point, existing Identities will be lost immediately.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "cache-mode-duration",
        "description": "Time limit for keeping Identities in the cache.",
        "type": "integer",
        "required": false,
        "valid_values": [
          "1-2880"
        ]
      },
      {
        "name": "remote-access",
        "description": "",
        "type": "array",
        "required": false,
        "default": "true",
        "valid_values": [
          "allowonlysinglelogintouser",
          "allowseverallogintouser"
        ]
      },
      {
        "name": "enable-back-connections",
        "description": "Usually communication with remote clients must be initialized by the clients. However, once a client has opened a connection, the hosts behind VPN can open a return or back connection to the client. For a back connection, the client's details must be maintained on all the devices between the client and the gateway, and on the gateway itself. Determine whether the back connection is enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "keep-alive-packet-to-gw-interval",
        "description": "Usually communication with remote clients must be initialized by the clients. However, once a client has opened a connection, the hosts behind VPN can open a return or back connection to the client. For a back connection, the client's details must be maintained on all the devices between the client and the gateway, and on the gateway itself. Determine frequency (in seconds) of the Keep Alive packets sent by the client in order to maintain the connection with the gateway.Available only if enable-back-connections is true.",
        "type": "integer",
        "required": false
      },
      {
        "name": "encrypt-dns-traffic",
        "description": "You can decide whether DNS queries sent by the remote client to a DNS server located on the corporate LAN are passed through the VPN tunnel or not. Disable this option if the client has to make DNS queries to the DNS server on the corporate LAN while connecting to the organization but without using the SecuRemote client.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "simultaneous-login-mode",
        "description": "Select the simultaneous login mode.",
        "type": "string",
        "required": false,
        "valid_values": [
          "allowonlysinglelogintouser",
          "allowseverallogintouser"
        ]
      },
      {
        "name": "vpn-authentication-and-encryption",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "true",
        "valid_values": [
          "AES-256",
          "DES",
          "AES-128",
          "3DES"
        ]
      },
      {
        "name": "encryption-algorithms",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "true",
        "valid_values": [
          "AES-256",
          "DES",
          "AES-128",
          "3DES"
        ]
      },
      {
        "name": "ike",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "true",
        "valid_values": [
          "AES-256",
          "DES",
          "AES-128",
          "3DES"
        ]
      },
      {
        "name": "support-encryption-algorithms",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "aes-128",
        "description": "Select whether the AES-128 encryption algorithm will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "aes-256",
        "description": "Select whether the AES-256 encryption algorithm will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "des",
        "description": "Select whether the DES encryption algorithm will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "tdes",
        "description": "Select whether the Triple DES encryption algorithm will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "use-encryption-algorithm",
        "description": "Choose the encryption algorithm that will have the highest priority of the selected algorithms. If given a choice of more that one encryption algorithm to use, the algorithm selected in this field will be used.",
        "type": "string",
        "required": false,
        "valid_values": [
          "AES-256",
          "DES",
          "AES-128",
          "3DES"
        ]
      },
      {
        "name": "support-data-integrity",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "aes-xcbc",
        "description": "Select whether the AES-XCBC hash algorithm will be supported with remote hosts to ensure data integrity.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "md5",
        "description": "Select whether the MD5 hash algorithm will be supported with remote hosts to ensure data integrity.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "sha1",
        "description": "Select whether the SHA1 hash algorithm will be supported with remote hosts to ensure data integrity.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "sha256",
        "description": "Select whether the SHA256 hash algorithm will be supported with remote hosts to ensure data integrity.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "sha384",
        "description": "Select whether the SHA384 hash algorithm will be supported with remote hosts to ensure data integrity.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "sha512",
        "description": "Select whether the SHA512 hash algorithm will be supported with remote hosts to ensure data integrity.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "use-data-integrity",
        "description": "The hash algorithm chosen here will be given the highest priority if more than one choice is offered.",
        "type": "string",
        "required": false,
        "valid_values": [
          "sha512",
          "sha384",
          "aes-xcbc",
          "sha256",
          "sha1",
          "md5"
        ]
      },
      {
        "name": "support-diffie-hellman-groups",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "true"
      },
      {
        "name": "group1",
        "description": "Select whether Diffie-Hellman Group 1 (768 bit) will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "group14",
        "description": "Select whether Diffie-Hellman Group 14 (2048 bit) will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "group15",
        "description": "Select whether Diffie-Hellman Group 15 (3072 bit) will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "group16",
        "description": "Select whether Diffie-Hellman Group 16 (4096 bit) will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "group17",
        "description": "Select whether Diffie-Hellman Group 17 (6144 bit) will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "group18",
        "description": "Select whether Diffie-Hellman Group 18 (8192 bit) will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "group19",
        "description": "Select whether Diffie-Hellman Group 19 (256-bit ECP) will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "group2",
        "description": "Select whether Diffie-Hellman Group 2 (1024 bit) will be supported with remote hosts.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "group20",
        "description": "Select whether Diffie-Hellman Group 20 (384-bit ECP) will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "group21",
        "description": "Select whether Diffie-Hellman Group 21 (521-bit ECP) will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "group5",
        "description": "Select whether Diffie-Hellman Group 5 (1536 bit) will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "use-diffie-hellman-group",
        "description": "SecureClient users utilize the Diffie-Hellman group selected in this field.",
        "type": "string",
        "required": false,
        "default": "Group 2",
        "valid_values": [
          "group 1",
          "group 2",
          "group 5",
          "group 14",
          "group 15",
          "group 16",
          "group 17",
          "group 18",
          "group 19",
          "group 20",
          "group 21"
        ]
      },
      {
        "name": "ipsec",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "AES-256",
          "DES",
          "AES-128",
          "3DES"
        ]
      },
      {
        "name": "support-encryption-algorithms",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "aes-128",
        "description": "Select whether the AES-128 encryption algorithm will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "aes-256",
        "description": "Select whether the AES-256 encryption algorithm will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "des",
        "description": "Select whether the DES encryption algorithm will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "tdes",
        "description": "Select whether the Triple DES encryption algorithm will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "use-encryption-algorithm",
        "description": "Choose the encryption algorithm that will have the highest priority of the selected algorithms. If given a choice of more that one encryption algorithm to use, the algorithm selected in this field will be used.",
        "type": "string",
        "required": false,
        "valid_values": [
          "AES-256",
          "DES",
          "AES-128",
          "3DES"
        ]
      },
      {
        "name": "support-data-integrity",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "aes-xcbc",
        "description": "Select whether the AES-XCBC hash algorithm will be supported with remote hosts to ensure data integrity.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "md5",
        "description": "Select whether the MD5 hash algorithm will be supported with remote hosts to ensure data integrity.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "sha1",
        "description": "Select whether the SHA1 hash algorithm will be supported with remote hosts to ensure data integrity.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "sha256",
        "description": "Select whether the SHA256 hash algorithm will be supported with remote hosts to ensure data integrity.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "sha384",
        "description": "Select whether the SHA384 hash algorithm will be supported with remote hosts to ensure data integrity.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "sha512",
        "description": "Select whether the SHA512 hash algorithm will be supported with remote hosts to ensure data integrity.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "use-data-integrity",
        "description": "The hash algorithm chosen here will be given the highest priority if more than one choice is offered.",
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
        "name": "enforce-encryption-alg-and-data-integrity-on-all-users",
        "description": "Enforce Encryption Algorithm and Data Integrity on all users.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "encryption-method",
        "description": "Select the encryption method.",
        "type": "string",
        "required": false,
        "default": "ike_v1_only",
        "valid_values": [
          "prefer_ikev2_support_ikev1",
          "ike_v2_only",
          "ike_v1_only"
        ]
      },
      {
        "name": "pre-shared-secret",
        "description": "the user password is specified in the Authentication tab in the user's IKE properties (in the user properties window: Encryption tab > Edit).",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "support-legacy-auth-for-sc-l2tp-nokia-clients",
        "description": "Support Legacy Authentication for SC (hybrid mode), L2TP (PAP) and Nokia clients (CRACK).",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "support-legacy-eap",
        "description": "Support Legacy EAP (Extensible Authentication Protocol).",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "support-l2tp-with-pre-shared-key",
        "description": "Use a centrally managed pre-shared key for IKE.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "l2tp-pre-shared-key",
        "description": "Type in the pre-shared key.Available only if support-l2tp-with-pre-shared-key is set to true.",
        "type": "string",
        "required": false
      },
      {
        "name": "vpn-advanced",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "true"
      },
      {
        "name": "allow-clear-traffic-to-encryption-domain-when-disconnected",
        "description": "SecuRemote/SecureClient behavior while disconnected - How traffic to the VPN domain is handled when the Remote Access VPN client is not connected to the site. Traffic can either be dropped or sent in clear without encryption.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "enable-load-distribution-for-mep-conf",
        "description": "Load distribution for Multiple Entry Points configurations - Remote access clients will randomly select a gateway from the list of entry points. Make sure to define the same VPN domain for all the Security Gateways you want to be entry points.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "use-first-allocated-om-ip-addr-for-all-conn-to-the-gws-of-the-site",
        "description": "Use first allocated Office Mode IP Address for all connections to the Gateways of the site.After a remote user connects and receives an Office Mode IP address from a gateway, every connection to that gateways encryption domain will go out with the Office Mode IP as the internal source IP. The Office Mode IP is what hosts in the encryption domain will recognize as the remote user's IP address. The Office Mode IP address assigned by a specific gateway can be used in its own encryption domain and in neighboring encryption domains as well. The neighboring encryption domains should reside behind gateways that are members of the same VPN community as the assigning gateway. Since the remote hosts connections are dependant on the Office Mode IP address it received, should the gateway that issued the IP become unavailable, all the connections to the site will terminate.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "scv",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "apply-scv-on-simplified-mode-fw-policies",
        "description": "Determine whether the gateway verifies that remote access clients are securely configured. This is set here only if the security policy is defined in the Simplified Mode. If the security policy is defined in the Traditional Mode, verification takes place per rule.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "exceptions",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "add",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "hosts",
        "description": "Specify the Hosts to be excluded from SCV.",
        "type": "string",
        "required": true
      },
      {
        "name": "services",
        "description": "Specify the services to be accessed.",
        "type": "string",
        "required": true
      },
      {
        "name": "hosts",
        "description": "Specify the Hosts to be excluded from SCV.",
        "type": "string",
        "required": true
      },
      {
        "name": "services",
        "description": "Specify the services to be accessed.",
        "type": "string",
        "required": true
      },
      {
        "name": "remove",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "hosts",
        "description": "Specify the Hosts to be excluded from SCV.",
        "type": "string",
        "required": true
      },
      {
        "name": "hosts",
        "description": "Specify the Hosts to be excluded from SCV.",
        "type": "string",
        "required": true
      },
      {
        "name": "hosts",
        "description": "Specify the Hosts to be excluded from SCV.",
        "type": "string",
        "required": true
      },
      {
        "name": "services",
        "description": "Specify the services to be accessed.",
        "type": "string",
        "required": true
      },
      {
        "name": "hosts",
        "description": "Specify the Hosts to be excluded from SCV.",
        "type": "string",
        "required": true
      },
      {
        "name": "services",
        "description": "Specify the services to be accessed.",
        "type": "string",
        "required": true
      },
      {
        "name": "no-scv-for-unsupported-cp-clients",
        "description": "Do not apply Secure Configuration Verification for connections from Check Point VPN clients that don't support it, such as SSL Network Extender, GO, Capsule VPN / Connect, Endpoint Connects lower than R75, or L2TP clients.Available only if apply-scv-on-simplified-mode-fw-policies is true.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "upon-verification-accept-and-log-client-connection",
        "description": "If the gateway verifies the client's configuration, decide how the gateway should handle connections with clients that fail the Security Configuration Verification. It is possible to either drop the connection or Accept the connection and log it.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "only-tcp-ip-protocols-are-used",
        "description": "Most SCV checks are configured via the SCV policy. Specify whether to verify that only TCP/IP protocols are used.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "policy-installed-on-all-interfaces",
        "description": "Most SCV checks are configured via the SCV policy. Specify whether to verify that the Desktop Security Policy is installed on all the interfaces of the client.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "generate-log",
        "description": "If the client identifies that the secure configuration has been violated, select whether a log is generated by the remote access client and sent to the Security Management server.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "notify-user",
        "description": "If the client identifies that the secure configuration has been violated, select whether to user should be notified.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "ssl-network-extender",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "legacy",
        "valid_values": [
          "certificate_with_enrollment",
          "certificate",
          "mixed",
          "legacy"
        ]
      },
      {
        "name": "user-auth-method",
        "description": "Wide Impact: Also applies for SecureClient Mobile devices and Check Point GO clients!User authentication method indicates how the user will be authenticated by the gateway. Changes made here will also apply for SSL clients.Legacy - Username and password only.Certificate - Certificate only with an existing certificate.Certificate with Enrollment - Allows you to obtain a new certificate and then use certificate authentication only.Mixed - Can use either username and password or certificate.",
        "type": "string",
        "required": false,
        "default": "legacy",
        "valid_values": [
          "certificate_with_enrollment",
          "certificate",
          "mixed",
          "legacy"
        ]
      },
      {
        "name": "supported-encryption-methods",
        "description": "Wide Impact: Also applies to SecureClient Mobile devices!Select the encryption algorithms that will be supported for remote users. Changes made here will also apply for all SSL clients.",
        "type": "string",
        "required": false,
        "default": "d3des_or_rc4",
        "valid_values": [
          "3des_or_rc4",
          "3des_only"
        ]
      },
      {
        "name": "client-upgrade-upon-connection",
        "description": "When a client connects to the gateway with SSL Network Extender, the client automatically checks for upgrade. Select whether the client should automatically upgrade.",
        "type": "string",
        "required": false,
        "default": "ask_user",
        "valid_values": [
          "force_upgrade",
          "ask_user",
          "no_upgrade"
        ]
      },
      {
        "name": "client-uninstall-upon-disconnection",
        "description": "Select whether the client should automatically uninstall SSL Network Extender when it disconnects from the gateway.",
        "type": "string",
        "required": false,
        "default": "dont_uninstall",
        "valid_values": [
          "force_uninstall",
          "ask_user",
          "dont_uninstall"
        ]
      },
      {
        "name": "re-auth-user-interval",
        "description": "Wide Impact: Applies for the SecureClient Mobile!Select the interval that users will need to reauthenticate.",
        "type": "integer",
        "required": false,
        "default": "480"
      },
      {
        "name": "scan-ep-machine-for-compliance-with-ep-compliance-policy",
        "description": "Set to true if you want endpoint machines to be scanned for compliance with the Endpoint Compliance Policy.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "client-outgoing-keep-alive-packets-frequency",
        "description": "Select the interval which the keep-alive packets are sent.",
        "type": "integer",
        "required": false,
        "default": "20"
      },
      {
        "name": "secure-client-mobile",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "legacy",
        "valid_values": [
          "certificate_with_enrollment",
          "certificate",
          "mixed",
          "legacy"
        ]
      },
      {
        "name": "user-auth-method",
        "description": "Wide Impact: Also applies for SSL Network Extender clients and Check Point GO clients.How the user will be authenticated by the gateway.",
        "type": "string",
        "required": false,
        "default": "legacy",
        "valid_values": [
          "certificate_with_enrollment",
          "certificate",
          "mixed",
          "legacy"
        ]
      },
      {
        "name": "enable-password-caching",
        "description": "If the password entered to authenticate is saved locally on the user's machine.",
        "type": "string",
        "required": false,
        "default": "false",
        "valid_values": [
          "client_decide",
          "true",
          "false"
        ]
      },
      {
        "name": "cache-password-timeout",
        "description": "Cached password timeout (in minutes).",
        "type": "integer",
        "required": false,
        "default": "1440"
      },
      {
        "name": "re-auth-user-interval",
        "description": "Wide Impact: Also applies for SSL Network Extender clients!The length of time (in minutes) until the user's credentials are resent to the gateway to verify authorization.",
        "type": "integer",
        "required": false,
        "default": "480"
      },
      {
        "name": "connect-mode",
        "description": "Methods by which a connection to the gateway will be initiated:Configured On Endpoint Client - the method used for initiating a connection to a gateway is determined by the endpoint clientManual - VPN connections will not be initiated automatically.Always connected - SecureClient Mobile will automatically establish a connection to the last connected gateway under the following circumstances: (a) the device has a valid IP address, (b) when the device \"wakes up\" from a low-power state or a soft-reset, or (c) after a condition that caused the device to automatically disconnect ceases to exist (for example, Device is out of PC Sync, Disconnect is not idle.).On application request - Applications requiring access to resources through the VPN will be able to initiate a VPN connection.",
        "type": "string",
        "required": false,
        "default": "Configured On Endpoint Client",
        "valid_values": [
          "manual",
          "always connected",
          "on application request",
          "configured on endpoint client"
        ]
      },
      {
        "name": "automatically-initiate-dialup",
        "description": "When selected, the client will initiate a GPRS dialup connection before attempting to establish the VPN connection. Note that if a local IP address is already available through another network interface, then the GPRS dialup is not initiated.",
        "type": "string",
        "required": false,
        "default": "client_decide",
        "valid_values": [
          "client_decide",
          "true",
          "false"
        ]
      },
      {
        "name": "disconnect-when-device-is-idle",
        "description": "Enabling this feature will disconnect users from the gateway if there is no traffic sent during the defined time period.",
        "type": "string",
        "required": false,
        "default": "client_decide",
        "valid_values": [
          "client_decide",
          "true",
          "false"
        ]
      },
      {
        "name": "supported-encryption-methods",
        "description": "Wide Impact: Also applies for SSL Network Extender clients!Select the encryption algorithms that will be supported with remote users.",
        "type": "string",
        "required": false,
        "default": "d3des_or_rc4",
        "valid_values": [
          "3des_or_rc4",
          "3des_only"
        ]
      },
      {
        "name": "route-all-traffic-to-gw",
        "description": "Operates the client in Hub Mode, sending all traffic to the VPN server for routing, filtering, and processing.",
        "type": "string",
        "required": false,
        "default": "false",
        "valid_values": [
          "client_decide",
          "true",
          "false"
        ]
      },
      {
        "name": "endpoint-connect",
        "description": "",
        "type": "array",
        "required": false,
        "default": "false",
        "valid_values": [
          "client_decide",
          "true",
          "false"
        ]
      },
      {
        "name": "enable-password-caching",
        "description": "If the password entered to authenticate is saved locally on the user's machine.",
        "type": "string",
        "required": false,
        "default": "false",
        "valid_values": [
          "client_decide",
          "true",
          "false"
        ]
      },
      {
        "name": "cache-password-timeout",
        "description": "Cached password timeout (in minutes).",
        "type": "integer",
        "required": false,
        "default": "1440"
      },
      {
        "name": "re-auth-user-interval",
        "description": "The length of time (in minutes) until the user's credentials are resent to the gateway to verify authorization.",
        "type": "integer",
        "required": false,
        "default": "480"
      },
      {
        "name": "connect-mode",
        "description": "Methods by which a connection to the gateway will be initiated:Manual - VPN connections will not be initiated automatically.Always connected - Endpoint Connect will automatically establish a connection to the last connected gateway under the following circumstances: (a) the device has a valid IP address, (b) when the device \"wakes up\" from a low-power state or a soft-reset, or (c) after a condition that caused the device to automatically disconnect ceases to exist (for example, Device is out of PC Sync, Disconnect is not idle.).Configured on endpoint client - the method used for initiating a connection to a gateway is determined by the endpoint client.",
        "type": "string",
        "required": false,
        "default": "Configured On Endpoint Client",
        "valid_values": [
          "Manual",
          "Always Connected",
          "Configured On Endpoint Client"
        ]
      },
      {
        "name": "network-location-awareness",
        "description": "Wide Impact: Also applies for Check Point GO clients!Endpoint Connect intelligently detects whether it is inside or outside of the VPN domain (Enterprise LAN), and automatically connects or disconnects as required. Select true and edit network-location-awareness-conf to configure this capability.",
        "type": "string",
        "required": false,
        "default": "client_decide",
        "valid_values": [
          "client_decide",
          "true",
          "false"
        ]
      },
      {
        "name": "network-location-awareness-conf",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "connects to gw through internal interface",
          "connects from network or group",
          "runs on computer with access to active directory domain"
        ]
      },
      {
        "name": "vpn-clients-are-considered-inside-the-internal-network-when-the-client",
        "description": "When a VPN client is within the internal network, the internal resources are available and the VPN tunnel should be disconnected. Determine when VPN clients are considered inside the internal network:Connects to GW through internal interface - The client connects to the gateway through one of its internal interfaces (recommended).Connects from network or group - The client connects from a network or group specified in network-or-group-of-conn-vpn-client.Runs on computer with access to Active Directory domain - The client runs on a computer that can access its Active Directory domain.Note: The VPN tunnel will resume automatically when the VPN client is no longer in the internal network and the client is set to \"Always connected\" mode.",
        "type": "string",
        "required": false,
        "valid_values": [
          "connects to gw through internal interface",
          "connects from network or group",
          "runs on computer with access to active directory domain"
        ]
      },
      {
        "name": "network-or-group-of-conn-vpn-client",
        "description": "Name or UID of Network or Group the VPN client is connected from.Available only if vpn-clients-are-considered-inside-the-internal-network-when-the-client is set to \"Connects from network or group\".",
        "type": "string",
        "required": false
      },
      {
        "name": "consider-wireless-networks-as-external",
        "description": "The speed at which locations are classified as internal or external can be increased by creating a list of wireless networks that are known to be external. A wireless network is identified by its Service Set Identifier (SSID) a name used to identify a particular 802.11 wireless LAN.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "excluded-internal-wireless-networks",
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
        "name": "consider-undefined-dns-suffixes-as-external",
        "description": "The speed at which locations are classified as internal or external can be increased by creating a list of DNS suffixes that are known to be external. Enable this to be able to define DNS suffixes which won't be considered external.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "dns-suffixes",
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
        "name": "remember-previously-detected-external-networks",
        "description": "The speed at which locations are classified as internal or external can be increased by caching (on the client side) names of networks that were previously determined to be external.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "disconnect-when-conn-to-network-is-lost",
        "description": "Enabling this feature disconnects users from the gateway when connectivity to the network is lost.",
        "type": "string",
        "required": false,
        "default": "client_decide",
        "valid_values": [
          "client_decide",
          "true",
          "false"
        ]
      },
      {
        "name": "disconnect-when-device-is-idle",
        "description": "Enabling this feature will disconnect users from the gateway if there is no traffic sent during the defined time period.",
        "type": "string",
        "required": false,
        "default": "client_decide",
        "valid_values": [
          "client_decide",
          "true",
          "false"
        ]
      },
      {
        "name": "route-all-traffic-to-gw",
        "description": "Operates the client in Hub Mode, sending all traffic to the VPN server for routing, filtering, and processing.",
        "type": "string",
        "required": false,
        "default": "false",
        "valid_values": [
          "client_decide",
          "true",
          "false"
        ]
      },
      {
        "name": "client-upgrade-mode",
        "description": "Select an option to determine how the client is upgraded.",
        "type": "string",
        "required": false,
        "default": "ask_user",
        "valid_values": [
          "force_upgrade",
          "ask_user",
          "no_upgrade"
        ]
      },
      {
        "name": "hot-spot-and-hotel-registration",
        "description": "",
        "type": "array",
        "required": false,
        "default": "600"
      },
      {
        "name": "enable-registration",
        "description": "Set Enable registration to true in order to configure settings. Set Enable registration to false in order to cancel registration (the configurations below won't be available). When the feature is enabled, you have several minutes to complete registration.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "local-subnets-access-only",
        "description": "Local subnets access only.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "registration-timeout",
        "description": "Maximum time (in seconds) to complete registration.",
        "type": "integer",
        "required": false,
        "default": "600"
      },
      {
        "name": "track-log",
        "description": "Track log.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "max-ip-access-during-registration",
        "description": "Maximum number of addresses to allow access to during registration.",
        "type": "integer",
        "required": false,
        "default": "5"
      },
      {
        "name": "ports",
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
        "name": "user-directory",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "true",
        "valid_values": [
          "no display",
          "display upon request",
          "display"
        ]
      },
      {
        "name": "enable-password-change-when-user-active-directory-expires",
        "description": "For organizations using MS Active Directory, this setting enables users whose passwords have expired to automatically create new passwords.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "cache-size",
        "description": "The maximum number of cached users allowed. The cache is FIFO (first-in, first-out). When a new user is added to a full cache, the first user is deleted to make room for the new user. The Check Point Security Gateway does not query the LDAP server for users already in the cache, unless the cache has timed out.",
        "type": "integer",
        "required": false,
        "default": "1000"
      },
      {
        "name": "enable-password-expiration-configuration",
        "description": "Enable configuring of the number of days during which the password is valid.If enable-password-change-when-user-active-directory-expires is true, the password expiration time is determined by the Active Directory. In this case it is recommended not to set this to true.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "password-expires-after",
        "description": "Specifies the number of days during which the password is valid. Users are authenticated using a special LDAP password. Should this password expire, a new password must be defined.Available only if enable-password-expiration-configuration is true.",
        "type": "integer",
        "required": false,
        "default": "90"
      },
      {
        "name": "timeout-on-cached-users",
        "description": "The period of time in which a cached user is timed out and will need to be fetched again from the LDAP server.",
        "type": "integer",
        "required": false,
        "default": "900"
      },
      {
        "name": "display-user-dn-at-login",
        "description": "Decide whether or not you would like to display the user's DN when logging in. If you choose to display the user DN, you can select whether to display it, when the user is prompted for the password at login, or on the request of the authentication scheme. This property is a useful diagnostic tool when there is more than one user with the same name in an Account Unit. In this case, the first one is chosen and the others are ignored.",
        "type": "string",
        "required": false,
        "default": "no display",
        "valid_values": [
          "no display",
          "display upon request",
          "display"
        ]
      },
      {
        "name": "enforce-rules-for-user-mgmt-admins",
        "description": "Enforces password strength rules on LDAP users when you create or modify a Check Point Password.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "min-password-length",
        "description": "Specifies the minimum length (in characters) of the password.",
        "type": "integer",
        "required": false,
        "default": "6"
      },
      {
        "name": "password-must-include-a-digit",
        "description": "Password must include a digit.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "password-must-include-a-symbol",
        "description": "Password must include a symbol.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "password-must-include-lowercase-char",
        "description": "Password must include a lowercase character.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "password-must-include-uppercase-char",
        "description": "Password must include an uppercase character.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "qos",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "10",
        "valid_values": [
          "bits-per-sec",
          "bytes-per-sec",
          "kbits-per-sec",
          "kbytes-per-sec",
          "mbits-per-sec",
          "mbytes-per-sec"
        ]
      },
      {
        "name": "default-weight-of-rule",
        "description": "Define a Weight at which bandwidth will be guaranteed. Set a default weight for a rule.Note: Value will be applied to new rules only.",
        "type": "integer",
        "required": false,
        "default": "10"
      },
      {
        "name": "max-weight-of-rule",
        "description": "Define a Weight at which bandwidth will be guaranteed. Set a maximum weight for a rule.",
        "type": "integer",
        "required": false,
        "default": "1000"
      },
      {
        "name": "unit-of-measure",
        "description": "Define the Rate at which packets are transmitted, for which bandwidth will be guaranteed. Set a Unit of measure.",
        "type": "string",
        "required": false,
        "default": "Kbits-per-sec",
        "valid_values": [
          "bits-per-sec",
          "bytes-per-sec",
          "kbits-per-sec",
          "kbytes-per-sec",
          "mbits-per-sec",
          "mbytes-per-sec"
        ]
      },
      {
        "name": "authenticated-ip-expiration",
        "description": "Define the Authentication time-out for QoS. This timeout is set in minutes. In an Authenticated IP all connections which are open in a specified time limit will be guaranteed bandwidth, but will not be guaranteed bandwidth after the time limit.",
        "type": "integer",
        "required": false,
        "default": "15"
      },
      {
        "name": "non-authenticated-ip-expiration",
        "description": "Define the Authentication time-out for QoS. This timeout is set in minutes.",
        "type": "integer",
        "required": false,
        "default": "5"
      },
      {
        "name": "unanswered-queried-ip-expiration",
        "description": "Define the Authentication time-out for QoS. This timeout is set in minutes.",
        "type": "integer",
        "required": false,
        "default": "3"
      },
      {
        "name": "carrier-security",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "true",
        "valid_values": [
          "before last",
          "last"
        ]
      },
      {
        "name": "block-gtp-in-gtp",
        "description": "Prevents GTP packets from being encapsulated inside GTP tunnels. When this option is checked, such packets are dropped and logged.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "enforce-gtp-anti-spoofing",
        "description": "verifies that G-PDUs are using the end user IP address that has been agreed upon in the PDP context activation process. When this option is checked, packets that do not use this IP address are dropped and logged.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "produce-extended-logs-on-unmatched-pdus",
        "description": "logs GTP packets not matched by previous rules with Carrier Security's extended GTP-related log fields. These logs are brown and their Action attribute is empty. The default setting is checked.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "produce-extended-logs-on-unmatched-pdus-position",
        "description": "Choose to place this implicit rule Before Last or as the Last rule.Available only if produce-extended-logs-on-unmatched-pdus is true.",
        "type": "string",
        "required": false,
        "default": "before last",
        "valid_values": [
          "before last",
          "last"
        ]
      },
      {
        "name": "protocol-violation-track-option",
        "description": "Set the appropriate track or alert option to be used when a protocol violation (malformed packet) is detected.",
        "type": "string",
        "required": false,
        "default": "log",
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
        "name": "enable-g-pdu-seq-number-check-with-max-deviation",
        "description": "If set to false, sequence checking is not enforced and all out-of-sequence G-PDUs will be accepted.To enhance performance, disable this extended integrity test.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "g-pdu-seq-number-check-max-deviation",
        "description": "specifies that a G-PDU is accepted only if the difference between its sequence number and the expected sequence number is less than or equal to the allowed deviation.Available only ifenable-g-pdu-seq-number-check-with-max-deviation is true.",
        "type": "integer",
        "required": false,
        "default": "16"
      },
      {
        "name": "verify-flow-labels",
        "description": "See that each packet's flow label matches the flow labels defined by GTP signaling. This option is relevant for GTP version 0 only.To enhance performance, disable this extended integrity test.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "allow-ggsn-replies-from-multiple-interfaces",
        "description": "Allows GTP signaling replies from an IP address different from the IP address to which the requests are sent (Relevant only for gateways below R80).",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "enable-reverse-connections",
        "description": "Allows Carrier Security gateways to accept PDUs sent from the GGSN to the SGSN, on a previously established PDP context, even if these PDUs are sent over ports that do not match the ports of the established PDP context.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "gtp-signaling-rate-limit-sampling-interval",
        "description": "Works in correlation with the property Enforce GTP Signal packet rate limit found in the Carrier Security window of the GSN network object. For example, with the rate limit sampling interval default of 1 second, and the network object enforced a GTP signal packet rate limit of the default 2048 PDU per second, sampling will occur one time per second, or 2048 signaling PDUs between two consecutive samplings.",
        "type": "integer",
        "required": false,
        "default": "1"
      },
      {
        "name": "one-gtp-echo-on-each-path-frequency",
        "description": "sets the number of GTP Echo exchanges per path allowed per configured time period. Echo requests exceeding this rate are dropped and logged. Setting the value to 0 disables the feature and allows an unlimited number of echo requests per path at any interval.",
        "type": "integer",
        "required": false,
        "default": "5"
      },
      {
        "name": "aggressive-aging",
        "description": "If true, enables configuring aggressive aging thresholds and time out value.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "aggressive-timeout",
        "description": "Aggressive timeout. Available only if aggressive-aging is true.",
        "type": "integer",
        "required": false,
        "default": "3600"
      },
      {
        "name": "memory-activation-threshold",
        "description": "Memory activation threshold. Available only if aggressive-aging is true.",
        "type": "integer",
        "required": false,
        "default": "80"
      },
      {
        "name": "memory-deactivation-threshold",
        "description": "Memory deactivation threshold. Available only if aggressive-aging is true.",
        "type": "integer",
        "required": false,
        "default": "60"
      },
      {
        "name": "tunnel-activation-threshold",
        "description": "Tunnel activation threshold. Available only if aggressive-aging is true.",
        "type": "integer",
        "required": false,
        "default": "80"
      },
      {
        "name": "tunnel-deactivation-threshold",
        "description": "Tunnel deactivation threshold. Available only if aggressive-aging is true.",
        "type": "integer",
        "required": false,
        "default": "60"
      },
      {
        "name": "user-accounts",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "expire after",
          "expire at"
        ]
      },
      {
        "name": "expiration-date-method",
        "description": "Select an Expiration Date Method.Expire at - Account expires on the date that you select.Expire after - Account expires after the number of days that you select.",
        "type": "string",
        "required": false,
        "valid_values": [
          "expire after",
          "expire at"
        ]
      },
      {
        "name": "expiration-date",
        "description": "Specify an Expiration Date in the following format: YYYY-MM-DD.Available only if expiration-date-method is set to \"expire at\".",
        "type": "string",
        "required": false
      },
      {
        "name": "days-until-expiration",
        "description": "Account expires after the number of days that you select.Available only if expiration-date-method is set to \"expire after\".",
        "type": "integer",
        "required": false
      },
      {
        "name": "show-accounts-expiration-indication-days-in-advance",
        "description": "Activates the Expired Accounts link, to open the Expired Accounts window.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "user-authority",
        "description": "",
        "type": "array",
        "required": false,
        "default": "all",
        "valid_values": [
          "selectively",
          "all"
        ]
      },
      {
        "name": "display-web-access-view",
        "description": "Specify whether or not to display the WebAccess rule base. This rule base is used for UserAuthority.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "windows-domains-to-trust",
        "description": "When matching Firewall usernames to Windows Domains usernames for Single Sign on, selectwhether to trust all or specify which Windows Domain should be trusted.ALL - Enables you to allow all Windows domains to access the internal sites of the organization.SELECTIVELY - Enables you to specify which Windows domains will have access to the internal sites of the organization.",
        "type": "string",
        "required": false,
        "default": "all",
        "valid_values": [
          "selectively",
          "all"
        ]
      },
      {
        "name": "trust-only-following-windows-domains",
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
        "name": "connect-control",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "18212"
      },
      {
        "name": "load-agents-port",
        "description": "Sets the port number on which load measuring agents communicate with ConnectControl.",
        "type": "integer",
        "required": false,
        "default": "18212"
      },
      {
        "name": "load-measurement-interval",
        "description": "sets how often (in seconds) the load measuring agents report their load status to ConnectControl.",
        "type": "integer",
        "required": false,
        "default": "20"
      },
      {
        "name": "persistence-server-timeout",
        "description": "Sets the amount of time (in seconds) that a client, once directed to a particular server, will continue to be directed to that same server.",
        "type": "integer",
        "required": false,
        "default": "1800"
      },
      {
        "name": "server-availability-check-interval",
        "description": "Sets how often (in seconds) ConnectControl checks to make sure the load balanced servers are running and responding to service requests.",
        "type": "integer",
        "required": false,
        "default": "20"
      },
      {
        "name": "server-check-retries",
        "description": "Sets how many times ConnectControl attempts to contact a server before ceasing to direct traffic to it.",
        "type": "integer",
        "required": false,
        "default": "3"
      },
      {
        "name": "stateful-inspection",
        "description": "",
        "type": "array",
        "required": false,
        "default": "25"
      },
      {
        "name": "tcp-start-timeout",
        "description": "A TCP connection will be timed out if the interval between the arrival of the first packet and establishment of the connection (TCP three-way handshake) exceeds TCP start timeout seconds.",
        "type": "integer",
        "required": false,
        "default": "25"
      },
      {
        "name": "tcp-session-timeout",
        "description": "The length of time (in seconds) an idle connection will remain in the Security Gateway connections table.",
        "type": "integer",
        "required": false,
        "default": "3600"
      },
      {
        "name": "tcp-end-timeout",
        "description": "A TCP connection will only terminate TCP end timeout seconds after two FIN packets (one in each direction: client-to-server, and server-to-client) or an RST packet. When a TCP connection ends (FIN packets sent or connection reset) the Check Point Security Gateway will keep the connection in the connections table for another TCP end timeout seconds, to allow for stray ACKs of the connection that arrive late.",
        "type": "integer",
        "required": false,
        "default": "20"
      },
      {
        "name": "tcp-end-timeout-r8020-gw-and-above",
        "description": "A TCP connection will only terminate TCP end timeout seconds after two FIN packets (one in each direction: client-to-server, and server-to-client) or an RST packet. When a TCP connection ends (FIN packets sent or connection reset) the Check Point Security Gateway will keep the connection in the connections table for another TCP end timeout seconds, to allow for stray ACKs of the connection that arrive late.",
        "type": "integer",
        "required": false,
        "default": "5"
      },
      {
        "name": "udp-virtual-session-timeout",
        "description": "Specifies the amount of time (in seconds) a UDP reply channel may remain open without any packets being returned.",
        "type": "integer",
        "required": false,
        "default": "40"
      },
      {
        "name": "icmp-virtual-session-timeout",
        "description": "An ICMP virtual session will be considered to have timed out after this time period (in seconds).",
        "type": "integer",
        "required": false,
        "default": "30"
      },
      {
        "name": "other-ip-protocols-virtual-session-timeout",
        "description": "A virtual session of services which are not explicitly configured here will be considered to have timed out after this time period (in seconds).",
        "type": "integer",
        "required": false,
        "default": "60"
      },
      {
        "name": "sctp-start-timeout",
        "description": "SCTP connections will be timed out if the interval between the arrival of the first packet and establishment of the connection exceeds this value (in seconds).",
        "type": "integer",
        "required": false,
        "default": "30"
      },
      {
        "name": "sctp-session-timeout",
        "description": "Time (in seconds) an idle connection will remain in the Security Gateway connections table.",
        "type": "integer",
        "required": false,
        "default": "3600"
      },
      {
        "name": "sctp-end-timeout",
        "description": "SCTP connections end after this number of seconds, after the connection ends or is reset, to allow for stray ACKs of the connection that arrive late.",
        "type": "integer",
        "required": false,
        "default": "20"
      },
      {
        "name": "accept-stateful-udp-replies-for-unknown-services",
        "description": "Specifies if UDP replies are to be accepted for unknown services.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "accept-stateful-icmp-errors",
        "description": "Accept ICMP error packets which refer to another non-ICMP connection (for example, to an ongoing TCP or UDP connection) that was accepted by the Rule Base.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "accept-stateful-icmp-replies",
        "description": "Accept ICMP reply packets for ICMP requests that were accepted by the Rule Base.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "accept-stateful-other-ip-protocols-replies-for-unknown-services",
        "description": "Accept reply packets for other undefined services (that is, services which are not one of the following: TCP, UDP, ICMP).",
        "type": "boolean",
        "required": false
      },
      {
        "name": "drop-out-of-state-tcp-packets",
        "description": "Drop TCP packets which are not consistent with the current state of the connection.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "log-on-drop-out-of-state-tcp-packets",
        "description": "Generates a log entry when these out of state TCP packets are dropped.Available only if drop-out-of-state-tcp-packets is true.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "tcp-out-of-state-drop-exceptions",
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
        "name": "drop-out-of-state-icmp-packets",
        "description": "Drop ICMP packets which are not consistent with the current state of the connection.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "log-on-drop-out-of-state-icmp-packets",
        "description": "Generates a log entry when these out of state ICMP packets are dropped.Available only if drop-out-of-state-icmp-packets is true.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "drop-out-of-state-sctp-packets",
        "description": "Drop SCTP packets which are not consistent with the current state of the connection.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "log-on-drop-out-of-state-sctp-packets",
        "description": "Generates a log entry when these out of state SCTP packets are dropped.Available only if drop-out-of-state-sctp-packets is true.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "log-and-alert",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "Log",
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
        "name": "administrative-notifications",
        "description": "Administrative notifications specifies the action to be taken when an administrative event (for example, when a certificate is about to expire) occurs.",
        "type": "string",
        "required": false,
        "default": "Log",
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
        "name": "connection-matched-by-sam",
        "description": "Connection matched by SAM specifies the action to be taken when a connection is blocked by SAM (Suspicious Activities Monitoring).",
        "type": "string",
        "required": false,
        "default": "Popup Alert",
        "valid_values": [
          "Popup Alert",
          "Mail Alert",
          "SNMP Trap Alert",
          "User Defined Alert no.1",
          "User Defined Alert no.2",
          "User Defined Alert no.3"
        ]
      },
      {
        "name": "dynamic-object-resolution-failure",
        "description": "Dynamic object resolution failure specifies the action to be taken when a dynamic object cannot be resolved.",
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
        "name": "ip-options-drop",
        "description": "IP Options drop specifies the action to take when a packet with IP Options is encountered. The Check Point Security Gateway always drops these packets, but you can log them or issue an alert.",
        "type": "string",
        "required": false,
        "default": "None",
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
        "name": "packet-is-incorrectly-tagged",
        "description": "Packet is incorrectly tagged.",
        "type": "string",
        "required": false,
        "default": "Log",
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
        "name": "packet-tagging-brute-force-attack",
        "description": "Packet tagging brute force attack.",
        "type": "string",
        "required": false,
        "default": "Popup Alert",
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
        "name": "sla-violation",
        "description": "SLA violation specifies the action to be taken when an SLA violation occurs, as defined in the Virtual Links window.",
        "type": "string",
        "required": false,
        "default": "None",
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
        "name": "vpn-conf-and-key-exchange-errors",
        "description": "VPN configuration & key exchange errors specifies the action to be taken when logging configuration or key exchange errors occur, for example, when attempting to establish encrypted communication with a network object inside the same encryption domain.",
        "type": "string",
        "required": false,
        "default": "Log",
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
        "name": "vpn-packet-handling-error",
        "description": "VPN packet handling errors specifies the action to be taken when encryption or decryption errors occurs. A log entry contains the action performed (Drop or Reject) and a short description of the error cause, for example, scheme or method mismatch.",
        "type": "string",
        "required": false,
        "default": "Log",
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
        "name": "vpn-successful-key-exchange",
        "description": "VPN successful key exchange specifies the action to be taken when VPN keys are successfully exchanged.",
        "type": "string",
        "required": false,
        "default": "Log",
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
        "name": "log-every-authenticated-http-connection",
        "description": "Log every authenticated HTTP connection specifies that a log entry should be generated for every authenticated HTTP connection.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "log-traffic",
        "description": "Log Traffic specifies whether or not to log traffic.",
        "type": "string",
        "required": false,
        "default": "Log",
        "valid_values": [
          "none",
          "log"
        ]
      },
      {
        "name": "alerts",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "true",
        "valid_values": [
          "Popup Alert",
          "Mail Alert",
          "SNMP Trap Alert",
          "User Defined Alert no.1",
          "User Defined Alert no.2",
          "User Defined Alert no.3"
        ]
      },
      {
        "name": "send-popup-alert-to-smartview-monitor",
        "description": "Send popup alert to SmartView Monitor when an alert is issued, it is also sent to SmartView Monitor.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "popup-alert-script",
        "description": "Run popup alert script the operating system script to be executed when an alert is issued. For example, set another form of notification, such as an email or a user-defined command.",
        "type": "string",
        "required": false
      },
      {
        "name": "send-mail-alert-to-smartview-monitor",
        "description": "Send mail alert to SmartView Monitor when a mail alert is issued, it is also sent to SmartView Monitor.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "mail-alert-script",
        "description": "Run mail alert script the operating system script to be executed when Mail is specified as the Track in a rule. The default is internal_sendmail, which is not a script but an internal Security Gateway command.",
        "type": "string",
        "required": false,
        "default": "internal_sendmail -s alert -t mailer root"
      },
      {
        "name": "send-snmp-trap-alert-to-smartview-monitor",
        "description": "Send SNMP trap alert to SmartView Monitor when an SNMP trap alert is issued, it is also sent to SmartView Monitor.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "snmp-trap-alert-script",
        "description": "Run SNMP trap alert script command to be executed when SNMP Trap is specified as the Track in a rule. By default the internal_snmp_trap is used. This command is executed by the fwd process.",
        "type": "string",
        "required": false,
        "default": "internal_snmp_trap localhost"
      },
      {
        "name": "send-user-defined-alert-num1-to-smartview-monitor",
        "description": "Send user defined alert no. 1 to SmartView Monitor when an alert is issued, it is also sent to SmartView Monitor.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "user-defined-script-num1",
        "description": "Run user defined script the operating system script to be run when User-Defined is specified as the Track in a rule, or when User Defined Alert no. 1 is selected as a Track Option.",
        "type": "string",
        "required": false
      },
      {
        "name": "send-user-defined-alert-num2-to-smartview-monitor",
        "description": "Send user defined alert no. 2 to SmartView Monitor when an alert is issued, it is also sent to SmartView Monitor.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "user-defined-script-num2",
        "description": "Run user defined 2 script the operating system script to be run when User-Defined is specified as the Track in a rule, or when User Defined Alert no. 2 is selected as a Track Option.",
        "type": "string",
        "required": false
      },
      {
        "name": "send-user-defined-alert-num3-to-smartview-monitor",
        "description": "Send user defined alert no. 3 to SmartView Monitor when an alert is issued, it is also sent to SmartView Monitor.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "user-defined-script-num3",
        "description": "Run user defined 3 script the operating system script to be run when User-Defined is specified as the Track in a rule, or when User Defined Alert no. 3 is selected as a Track Option.",
        "type": "string",
        "required": false
      },
      {
        "name": "default-track-option-for-system-alerts",
        "description": "Set the default track option for System Alerts.",
        "type": "string",
        "required": false,
        "default": "Popup Alert",
        "valid_values": [
          "Popup Alert",
          "Mail Alert",
          "SNMP Trap Alert",
          "User Defined Alert no.1",
          "User Defined Alert no.2",
          "User Defined Alert no.3"
        ]
      },
      {
        "name": "time-settings",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "62"
      },
      {
        "name": "excessive-log-grace-period",
        "description": "Specifies the minimum amount of time (in seconds) between consecutive logs of similar packets. Two packets are considered similar if they have the same source address, source port, destination address, and destination port; and the same protocol was used. After the first packet, similar packets encountered in the grace period will be acted upon according to the security policy, but only the first packet generates a log entry or an alert. Any value from 0 to 90 seconds can be entered in this field.Note: This option only applies for DROP rules with logging.",
        "type": "integer",
        "required": false,
        "default": "62"
      },
      {
        "name": "logs-resolving-timeout",
        "description": "Specifies the amount of time (in seconds), after which the log page is displayed without resolving names and while showing only IP addresses. Any value from 0 to 90 seconds can be entered in this field.",
        "type": "integer",
        "required": false,
        "default": "20"
      },
      {
        "name": "status-fetching-interval",
        "description": "Specifies the frequency at which the Security Management server queries the Check Point Security gateway, Check Point QoS and other gateways it manages for status information. Any value from 30 to 900 seconds can be entered in this field.",
        "type": "integer",
        "required": false,
        "default": "60"
      },
      {
        "name": "virtual-link-statistics-logging-interval",
        "description": "Specifies the frequency (in seconds) with which Virtual Link statistics will be logged. This parameter is relevant only for Virtual Links defined with SmartView Monitor statistics enabled in the SLA Parameters tab of the Virtual Link window. Any value from 60 to 3600 seconds can be entered in this field.",
        "type": "integer",
        "required": false,
        "default": "60"
      },
      {
        "name": "data-access-control",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "true"
      },
      {
        "name": "auto-download-important-data",
        "description": "Automatically download and install Software Blade Contracts, security updates and other important data (highly recommended).",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "auto-download-sw-updates-and-new-features",
        "description": "Automatically download software updates and new features (highly recommended).Available only if auto-download-important-data is set to true.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "send-anonymous-info",
        "description": "Help Check Point improve the product by sending anonymous information.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "share-sensitive-info",
        "description": "Approve sharing core dump files and other relevant crash data which might contain personal information. All shared data will be processed in accordance with Check Point's Privacy Policy.Available only if send-anonymous-info is set to true.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "non-unique-ip-address-ranges",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "IPv4",
          "IPv6"
        ]
      },
      {
        "name": "add",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "IPv4",
          "IPv6"
        ]
      },
      {
        "name": "address-type",
        "description": "The type of the IP Address.",
        "type": "string",
        "required": true,
        "valid_values": [
          "IPv4",
          "IPv6"
        ]
      },
      {
        "name": "first-ipv4-address",
        "description": "The first IPV4 Address in the range.",
        "type": "string",
        "required": true
      },
      {
        "name": "last-ipv4-address",
        "description": "The last IPV4 Address in the range.",
        "type": "string",
        "required": true
      },
      {
        "name": "address-type",
        "description": "The type of the IP Address.",
        "type": "string",
        "required": true,
        "valid_values": [
          "IPv4",
          "IPv6"
        ]
      },
      {
        "name": "first-ipv4-address",
        "description": "The first IPV4 Address in the range.",
        "type": "string",
        "required": true
      },
      {
        "name": "last-ipv4-address",
        "description": "The last IPV4 Address in the range.",
        "type": "string",
        "required": true
      },
      {
        "name": "remove",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "IPv4",
          "IPv6"
        ]
      },
      {
        "name": "address-type",
        "description": "The type of the IP Address.",
        "type": "string",
        "required": true,
        "valid_values": [
          "IPv4",
          "IPv6"
        ]
      },
      {
        "name": "first-ipv4-address",
        "description": "The first IPV4 Address in the range.",
        "type": "string",
        "required": true
      },
      {
        "name": "last-ipv4-address",
        "description": "The last IPV4 Address in the range.",
        "type": "string",
        "required": true
      },
      {
        "name": "address-type",
        "description": "The type of the IP Address.",
        "type": "string",
        "required": true,
        "valid_values": [
          "IPv4",
          "IPv6"
        ]
      },
      {
        "name": "first-ipv4-address",
        "description": "The first IPV4 Address in the range.",
        "type": "string",
        "required": true
      },
      {
        "name": "last-ipv4-address",
        "description": "The last IPV4 Address in the range.",
        "type": "string",
        "required": true
      },
      {
        "name": "address-type",
        "description": "The type of the IP Address.",
        "type": "string",
        "required": true,
        "valid_values": [
          "IPv4",
          "IPv6"
        ]
      },
      {
        "name": "first-ipv4-address",
        "description": "The first IPV4 Address in the range.",
        "type": "string",
        "required": true
      },
      {
        "name": "last-ipv4-address",
        "description": "The last IPV4 Address in the range.",
        "type": "string",
        "required": true
      },
      {
        "name": "address-type",
        "description": "The type of the IP Address.",
        "type": "string",
        "required": true,
        "valid_values": [
          "IPv4",
          "IPv6"
        ]
      },
      {
        "name": "first-ipv4-address",
        "description": "The first IPV4 Address in the range.",
        "type": "string",
        "required": true
      },
      {
        "name": "last-ipv4-address",
        "description": "The last IPV4 Address in the range.",
        "type": "string",
        "required": true
      },
      {
        "name": "proxy",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "false"
      },
      {
        "name": "use-proxy-server",
        "description": "If set to true, a proxy server is used when features need to access the internet.",
        "type": "boolean",
        "required": false,
        "default": "false"
      },
      {
        "name": "proxy-address",
        "description": "Specify the URL or IP address of the proxy server.Available only if use-proxy-server is set to true.",
        "type": "string",
        "required": false
      },
      {
        "name": "proxy-port",
        "description": "Specify the Port on which the server will be accessed.Available only if use-proxy-server is set to true.",
        "type": "integer",
        "required": false,
        "default": "80"
      },
      {
        "name": "user-check",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "English",
        "valid_values": [
          "Afrikaans",
          "Albanian",
          "Amharic",
          "Arabic",
          "Armenian",
          "Basque",
          "Belarusian",
          "Bosnian",
          "Bulgarian",
          "Catalan",
          "Chinese",
          "Croatian",
          "Czech",
          "Danish",
          "Dutch",
          "English",
          "Estonian",
          "Finnish",
          "French",
          "Gaelic",
          "Georgian",
          "German",
          "Greek",
          "Hebrew",
          "Hindi",
          "Hungarian",
          "Icelandic",
          "Indonesian",
          "Irish",
          "Italian",
          "Japanese",
          "Korean",
          "Latvian",
          "Lithuanian",
          "Macedonia",
          "Maltese",
          "Nepali",
          "Norwegian",
          "Polish",
          "Portuguese",
          "Romanian",
          "Russian",
          "Serbian",
          "Slovak",
          "Slovenian",
          "Sorbian",
          "Spanish",
          "Swahili",
          "Swedish",
          "Thai",
          "Turkish",
          "Ukrainian",
          "Vietnamese",
          "Welsh"
        ]
      },
      {
        "name": "preferred-language",
        "description": "The preferred language for new UserCheck message.",
        "type": "string",
        "required": false,
        "default": "English",
        "valid_values": [
          "Afrikaans",
          "Albanian",
          "Amharic",
          "Arabic",
          "Armenian",
          "Basque",
          "Belarusian",
          "Bosnian",
          "Bulgarian",
          "Catalan",
          "Chinese",
          "Croatian",
          "Czech",
          "Danish",
          "Dutch",
          "English",
          "Estonian",
          "Finnish",
          "French",
          "Gaelic",
          "Georgian",
          "German",
          "Greek",
          "Hebrew",
          "Hindi",
          "Hungarian",
          "Icelandic",
          "Indonesian",
          "Irish",
          "Italian",
          "Japanese",
          "Korean",
          "Latvian",
          "Lithuanian",
          "Macedonia",
          "Maltese",
          "Nepali",
          "Norwegian",
          "Polish",
          "Portuguese",
          "Romanian",
          "Russian",
          "Serbian",
          "Slovak",
          "Slovenian",
          "Sorbian",
          "Spanish",
          "Swahili",
          "Swedish",
          "Thai",
          "Turkish",
          "Ukrainian",
          "Vietnamese",
          "Welsh"
        ]
      },
      {
        "name": "send-emails-using-mail-server",
        "description": "Name or UID of mail server to send emails to.",
        "type": "string",
        "required": false
      },
      {
        "name": "hit-count",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "true",
        "valid_values": [
          "3 months",
          "6 months",
          "1 year",
          "2 years"
        ]
      },
      {
        "name": "enable-hit-count",
        "description": "Select to enable or clear to disable all Security Gateways to monitor the number of connections each rule matches.",
        "type": "boolean",
        "required": false,
        "default": "true"
      },
      {
        "name": "keep-hit-count-data-up-to",
        "description": "Select one of the time range options. Data is kept in the Security Management Server database for this period and is shown in the Hits column.",
        "type": "string",
        "required": false,
        "default": "3 Months",
        "valid_values": [
          "3 months",
          "6 months",
          "1 year",
          "2 years"
        ]
      },
      {
        "name": "advanced-conf",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "off",
        "valid_values": [
          "off",
          "alert",
          "fail"
        ]
      },
      {
        "name": "certs-and-pki",
        "description": "",
        "type": "Object",
        "required": false,
        "default": "off",
        "valid_values": [
          "off",
          "alert",
          "fail"
        ]
      },
      {
        "name": "cert-validation-enforce-key-size",
        "description": "Enforce key length in certificate validation (R80+ gateways only).",
        "type": "string",
        "required": false,
        "default": "off",
        "valid_values": [
          "off",
          "alert",
          "fail"
        ]
      },
      {
        "name": "host-certs-ecdsa-key-size",
        "description": "Select the key size for ECDSA of the host certificate.",
        "type": "string",
        "required": false,
        "default": "P-256",
        "valid_values": [
          "p-256",
          "p-384",
          "p-521"
        ]
      },
      {
        "name": "host-certs-key-size",
        "description": "Select the key size of the host certificate.",
        "type": "string",
        "required": false,
        "default": "2048",
        "valid_values": [
          "4096",
          "1024",
          "2048",
          "3072"
        ]
      },
      {
        "name": "keep-ike-sas",
        "description": "Enabled: Keep ALL IKEv1 phase 1 Security Associations (SA) upon policy installation.Disabled: Delete ALL IKEv1 phase 1 Security Associations (SA) upon policy installation.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "allow-remote-registration-of-opsec-products",
        "description": "After installing an OPSEC application, the remote administration (RA) utility enables an OPSEC product to finish registering itself without having to access the SmartConsole. If set to true, any host including the application host can run the utility. Otherwise, the RA utility can only be run from the Security Management host.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "num-spoofing-errs-that-trigger-brute-force",
        "description": "Indicates how many incorrectly signed packets will be tolerated before assuming that there is an attack on the packet tagging and revoking the client's key.",
        "type": "integer",
        "required": false,
        "default": "3"
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
        "name": "firewall",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "first",
          "last",
          "before last"
        ]
      },
      {
        "name": "accept-control-connections",
        "description": "Used for: Installing the security policy from the Security Management server to the gateways. Sending logs from the gateways to the Security Management server. Communication between SmartConsole clients and the Security Management Server Communication between Firewall daemons on different machines (Security Management Server, Security Gateway). Connecting to OPSEC applications such as RADIUS and TACACS authentication servers.If you disable Accept Control Connections and you want Check Point components to communicate with each other and with OPSEC components, you must explicitly allow these connections in the Rule Base.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "accept-control-connections-position",
        "description": "The position of the implied rules in the Rule Base.",
        "type": "string",
        "required": false,
        "valid_values": [
          "first",
          "last",
          "before last"
        ]
      },
      {
        "name": "accept-ips1-management-connections",
        "description": "Accepts IPS-1 connections.Available only if accept-control-connections is true.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "accept-ips1-management-connections-position",
        "description": "The position of the implied rules in the Rule Base.",
        "type": "string",
        "required": false,
        "valid_values": [
          "first",
          "last",
          "before last"
        ]
      },
      {
        "name": "accept-remote-access-control-connections",
        "description": "Accepts Remote Access connections.Available only if accept-control-connections is true.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "accept-remote-access-control-connections-position",
        "description": "The position of the implied rules in the Rule Base.",
        "type": "string",
        "required": false,
        "valid_values": [
          "first",
          "last",
          "before last"
        ]
      },
      {
        "name": "accept-smart-update-connections",
        "description": "Accepts SmartUpdate connections.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "accept-smart-update-connections-position",
        "description": "The position of the implied rules in the Rule Base.",
        "type": "string",
        "required": false,
        "valid_values": [
          "first"
        ]
      },
      {
        "name": "accept-outgoing-packets-originating-from-gw",
        "description": "Accepts all packets from connections that originate at the Check Point Security Gateway.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "accept-outgoing-packets-originating-from-gw-position",
        "description": "The position of the implied rules in the Rule Base.Available only if accept-outgoing-packets-originating-from-gw is false.",
        "type": "string",
        "required": false,
        "valid_values": [
          "first",
          "last",
          "before last"
        ]
      },
      {
        "name": "accept-outgoing-packets-originating-from-connectra-gw",
        "description": "Accepts outgoing packets originating from Connectra gateway.Available only if accept-outgoing-packets-originating-from-gw is false.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "accept-outgoing-packets-to-cp-online-services",
        "description": "Allow Security Gateways to access Check Point online services. Supported for R80.10 Gateway and higher.Available only if accept-outgoing-packets-originating-from-gw is false.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "accept-outgoing-packets-to-cp-online-services-position",
        "description": "The position of the implied rules in the Rule Base.Available only if accept-outgoing-packets-to-cp-online-services is true.",
        "type": "string",
        "required": false,
        "valid_values": [
          "first",
          "last",
          "before last"
        ]
      },
      {
        "name": "accept-domain-name-over-tcp",
        "description": "Accepts Domain Name (DNS) queries and replies over TCP, to allow downloading of the domain name-resolving tables used for zone transfers between servers. For clients, DNS over TCP is only used if the tables to be transferred are very large.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "accept-domain-name-over-tcp-position",
        "description": "The position of the implied rules in the Rule Base.Available only if accept-domain-name-over-tcp is true.",
        "type": "string",
        "required": false,
        "valid_values": [
          "first",
          "last",
          "before last"
        ]
      },
      {
        "name": "accept-domain-name-over-udp",
        "description": "Accepts Domain Name (DNS) queries and replies over UDP.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "accept-domain-name-over-udp-position",
        "description": "The position of the implied rules in the Rule Base.Available only if accept-domain-name-over-udp is true.",
        "type": "string",
        "required": false,
        "valid_values": [
          "first",
          "last",
          "before last"
        ]
      },
      {
        "name": "accept-dynamic-addr-modules-outgoing-internet-connections",
        "description": "Accept Dynamic Address modules' outgoing internet connections.Accepts DHCP traffic for DAIP (Dynamically Assigned IP Address) gateways. In Small Office Appliance gateways, this rule allows outgoing DHCP, PPP, PPTP and L2TP Internet connections (regardless of whether it is or is not a DAIP gateway).",
        "type": "boolean",
        "required": false
      },
      {
        "name": "accept-dynamic-addr-modules-outgoing-internet-connections-position",
        "description": "The position of the implied rules in the Rule Base.Available only if accept-dynamic-addr-modules-outgoing-internet-connections is true.",
        "type": "string",
        "required": false,
        "valid_values": [
          "first"
        ]
      },
      {
        "name": "accept-icmp-requests",
        "description": "Accepts Internet Control Message Protocol messages.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "accept-icmp-requests-position",
        "description": "The position of the implied rules in the Rule Base.Available only if accept-icmp-requests is true.",
        "type": "string",
        "required": false,
        "valid_values": [
          "first",
          "last",
          "before last"
        ]
      },
      {
        "name": "accept-identity-awareness-control-connections",
        "description": "Accepts traffic between Security Gateways in distributed environment configurations of Identity Awareness.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "accept-identity-awareness-control-connections-position",
        "description": "The position of the implied rules in the Rule Base.Available only if accept-identity-awareness-control-connections is true.",
        "type": "string",
        "required": false,
        "valid_values": [
          "first",
          "last",
          "before last"
        ]
      },
      {
        "name": "accept-incoming-traffic-to-dhcp-and-dns-services-of-gws",
        "description": "Allows the Small Office Appliance gateway to provide DHCP relay, DHCP server and DNS proxy services regardless of the rule base.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "accept-incoming-traffic-to-dhcp-and-dns-services-of-gws-position",
        "description": "The position of the implied rules in the Rule Base.Available only if accept-incoming-traffic-to-dhcp-and-dns-services-of-gws is true.",
        "type": "string",
        "required": false,
        "valid_values": [
          "first",
          "last",
          "before last"
        ]
      },
      {
        "name": "accept-rip",
        "description": "Accepts Routing Information Protocol (RIP), using UDP on port 520.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "accept-rip-position",
        "description": "The position of the implied rules in the Rule Base.Available only if accept-rip is true.",
        "type": "string",
        "required": false,
        "valid_values": [
          "first",
          "last",
          "before last"
        ]
      },
      {
        "name": "accept-vrrp-packets-originating-from-cluster-members",
        "description": "Selecting this option creates an implied rule in the security policy Rule Base that accepts VRRP inbound and outbound traffic to and from the members of the cluster.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "accept-vrrp-packets-originating-from-cluster-members-position",
        "description": "The position of the implied rules in the Rule Base.Available only if accept-vrrp-packets-originating-from-cluster-members is true.",
        "type": "string",
        "required": false,
        "valid_values": [
          "first",
          "last",
          "before last"
        ]
      },
      {
        "name": "accept-web-and-ssh-connections-for-gw-administration",
        "description": "Accepts Web and SSH connections for Small Office Appliance gateways.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "accept-web-and-ssh-connections-for-gw-administration-position",
        "description": "The position of the implied rules in the Rule Base.Available only if accept-web-and-ssh-connections-for-gw-administration is true.",
        "type": "string",
        "required": false,
        "valid_values": [
          "first",
          "last",
          "before last"
        ]
      },
      {
        "name": "log-implied-rules",
        "description": "Produces log records for communications that match the implied rules that are generated in the Rule Base from the properties defined in this window.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "security-server",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "standard",
          "post request",
          "every request"
        ]
      },
      {
        "name": "client-auth-welcome-file",
        "description": "Client authentication welcome file is the name of a file whose contents are to be displayed when a user begins a Client Authenticated session (optional) using the Manual Sign On Method. Client Authenticated Sessions initiated by Manual Sign On are not mediated by a security server.",
        "type": "string",
        "required": false
      },
      {
        "name": "ftp-welcome-msg-file",
        "description": "FTP welcome message file is the name of a file whose contents are to be displayed when a user begins an Authenticated FTP session.",
        "type": "string",
        "required": false
      },
      {
        "name": "rlogin-welcome-msg-file",
        "description": "Rlogin welcome message file is the name of a file whose contents are to be displayed when a user begins an Authenticated RLOGIN session.",
        "type": "string",
        "required": false
      },
      {
        "name": "telnet-welcome-msg-file",
        "description": "Telnet welcome message file is the name of a file whose contents are to be displayed when a user begins an Authenticated Telnet session.",
        "type": "string",
        "required": false
      },
      {
        "name": "mdq-welcome-msg",
        "description": "MDQ Welcome Message is the message to be displayed when a user begins an MDQ session. The MDQ Welcome Message should contain characters according to RFC 1035 and it must follow the ARPANET host name rules: - This message must begin with a number or letter. After the first letter or number character the remaining characters can be a letter, number, space, tab or hyphen. - This message must not end with a space or a tab and is limited to 63 characters.",
        "type": "string",
        "required": false
      },
      {
        "name": "smtp-welcome-msg",
        "description": "SMTP Welcome Message is the message to be displayed when a user begins an SMTP session.",
        "type": "string",
        "required": false
      },
      {
        "name": "http-servers",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "standard",
          "post request",
          "every request"
        ]
      },
      {
        "name": "logical-name",
        "description": "Unique Logical Name of the HTTP Server.",
        "type": "string",
        "required": false
      },
      {
        "name": "host",
        "description": "Host name of the HTTP Server.",
        "type": "string",
        "required": false
      },
      {
        "name": "port",
        "description": "Port number of the HTTP Server.",
        "type": "integer",
        "required": false
      },
      {
        "name": "reauthentication",
        "description": "Specify whether users must reauthenticate when accessing a specific server.",
        "type": "string",
        "required": false,
        "valid_values": [
          "standard",
          "post request",
          "every request"
        ]
      },
      {
        "name": "server-for-null-requests",
        "description": "The Logical Name of a Null Requests Server from http-servers.",
        "type": "string",
        "required": false
      },
      {
        "name": "identity-awareness",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "cache-mode",
        "description": "True: In case of connectivity loss from the Policy-Decision-Point (PDP), extend Identity cache up-to \"cache-mode-duration\".False: Identity Cache Mode is disabled, in case of connectivity loss from the Policy-Decision-Point, existing Identities will be lost immediately.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "cache-mode-duration",
        "description": "Time limit for keeping Identities in the cache.",
        "type": "integer",
        "required": false
      },
      {
        "name": "nat",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "ip allocation log",
          "none"
        ]
      },
      {
        "name": "allow-bi-directional-nat",
        "description": "Applies to automatic NAT rules in the NAT Rule Base, and allows two automatic NAT rules to match a connection. Without Bidirectional NAT, only one automatic NAT rule can match a connection.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "auto-arp-conf",
        "description": "Ensures that ARP requests for a translated (NATed) machine, network or address range are answered by the Check Point Security Gateway.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "merge-manual-proxy-arp-conf",
        "description": "Merges the automatic and manual ARP configurations. Manual proxy ARP configuration is required for manual Static NAT rules.Available only if auto-arp-conf is true.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "auto-translate-dest-on-client-side",
        "description": "Applies to packets originating at the client, with the server as its destination. Static NAT for the server is performed on the client side.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "manually-translate-dest-on-client-side",
        "description": "Applies to packets originating at the client, with the server as its destination. Static NAT for the server is performed on the client side.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "enable-ip-pool-nat",
        "description": "Applies to packets originating at the client, with the server as its destination. Static NAT for the server is performed on the client side.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "addr-alloc-and-release-track",
        "description": "Specifies whether to log each allocation and release of an IP address from the IP Pool.Available only if enable-ip-pool-nat is true.",
        "type": "string",
        "required": false,
        "valid_values": [
          "ip allocation log",
          "none"
        ]
      },
      {
        "name": "addr-exhaustion-track",
        "description": "Specifies the action to take if the IP Pool is exhausted.Available only if enable-ip-pool-nat is true.",
        "type": "string",
        "required": false,
        "valid_values": [
          "ip exhaustion alert",
          "none",
          "ip exhaustion log"
        ]
      },
      {
        "name": "authentication",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "auth-internal-users-with-specific-suffix",
        "description": "Enforce suffix for internal users authentication.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "allowed-suffix-for-internal-users",
        "description": "Suffix for internal users authentication.",
        "type": "string",
        "required": false
      },
      {
        "name": "max-days-before-expiration-of-non-pulled-user-certificates",
        "description": "Users certificates which were initiated but not pulled will expire after the specified number of days. Any value from 1 to 60 days can be entered in this field.",
        "type": "integer",
        "required": false
      },
      {
        "name": "max-client-auth-attempts-before-connection-termination",
        "description": "Allowed Number of Failed Client Authentication Attempts Before Session Termination. Any value from 1 to 800 attempts can be entered in this field.",
        "type": "integer",
        "required": false
      },
      {
        "name": "max-rlogin-attempts-before-connection-termination",
        "description": "Allowed Number of Failed rlogin Attempts Before Session Termination. Any value from 1 to 800 attempts can be entered in this field.",
        "type": "integer",
        "required": false
      },
      {
        "name": "max-session-auth-attempts-before-connection-termination",
        "description": "Allowed Number of Failed Session Authentication Attempts Before Session Termination. Any value from 1 to 800 attempts can be entered in this field.",
        "type": "integer",
        "required": false
      },
      {
        "name": "max-telnet-attempts-before-connection-termination",
        "description": "Allowed Number of Failed telnet Attempts Before Session Termination. Any value from 1 to 800 attempts can be entered in this field.",
        "type": "integer",
        "required": false
      },
      {
        "name": "enable-delayed-auth",
        "description": "all authentications other than certificate-based authentications will be delayed by the specified time. Applying this delay will stall brute force authentication attacks. The delay is applied for both failed and successful authentication attempts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "delay-each-auth-attempt-by",
        "description": "Delay each authentication attempt by the specified number of milliseconds. Any value from 1 to 25000 can be entered in this field.",
        "type": "integer",
        "required": false
      },
      {
        "name": "vpn",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "simplified",
          "traditional",
          "per policy"
        ]
      },
      {
        "name": "vpn-conf-method",
        "description": "Decide on Simplified or Traditional mode for all new security policies or decide which mode to use on a policy by policy basis.",
        "type": "string",
        "required": false,
        "valid_values": [
          "simplified",
          "traditional",
          "per policy"
        ]
      },
      {
        "name": "domain-name-for-dns-resolving",
        "description": "Enter the domain name that will be used for gateways DNS lookup. The DNS host name that is used is \"gateway_name.domain_name\".",
        "type": "string",
        "required": false
      },
      {
        "name": "enable-backup-gw",
        "description": "Enable Backup Gateway.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "enable-decrypt-on-accept-for-gw-to-gw-traffic",
        "description": "Enable decrypt on accept for gateway to gateway traffic. This is only relevant for policies in traditional mode. In Traditional Mode, the 'Accept' action determines that a connection is allowed, while the 'Encrypt' action determines that a connection is allowed and encrypted. Select whether VPN accepts an encrypted packet that matches a rule with an 'Accept' action or drops it.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "enable-load-distribution-for-mep-conf",
        "description": "Enable load distribution for Multiple Entry Points configurations (Site To Site connections). The VPN Multiple Entry Point (MEP) feature supplies high availability and load distribution for Check Point Security Gateways. MEP works in four modes: First to Respond, in which the first gateway to reply to the peer gateway is chosen. An organization would choose this option if, for example, the organization has two gateways in a MEPed configuration - one in London, the other in New York. It makes sense for Check Point Security Gateway peers located in England to try the London gateway first and the NY gateway second. Being geographically closer to Check Point Security Gateway peers in England, the London gateway will be the first to respond, and becomes the entry point to the internal network. VPN Domain, is when the destination IP belongs to a particular VPN domain, the gateway of that domain becomes the chosen entry point. This gateway becomes the primary gateway while other gateways in the MEP configuration become its backup gateways. Random Selection, in which the remote Check Point Security Gateway peer randomly selects a gateway with which to open a VPN connection. For each IP source/destination address pair, a new gateway is randomly selected. An organization might have a number of machines with equal performance abilities. In this case, it makes sense to enable load distribution. The machines are used in a random and equal way. Manually set priority list, gateway priorities can be set manually for the entire community or for individual satellite gateways..",
        "type": "boolean",
        "required": false
      },
      {
        "name": "enable-vpn-directional-match-in-vpn-column",
        "description": "Enable VPN Directional Match in VPN Column.Note: VPN Directional Match is supported only on Gaia, SecurePlatform, Linux and IPSO.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "grace-period-after-the-crl-is-not-valid",
        "description": "When establishing VPN tunnels, the peer presents its certificate for authentication. The clock on the gateway machine must be synchronized with the clock on the Certificate Authority machine. Otherwise, the Certificate Revocation List (CRL) used for validating the peer's certificate may be considered invalid and thus the authentication fails. To resolve the issue of differing clock times, a Grace Period permits a wider window for CRL validity.",
        "type": "integer",
        "required": false
      },
      {
        "name": "grace-period-before-the-crl-is-valid",
        "description": "When establishing VPN tunnels, the peer presents its certificate for authentication. The clock on the gateway machine must be synchronized with the clock on the Certificate Authority machine. Otherwise, the Certificate Revocation List (CRL) used for validating the peer's certificate may be considered invalid and thus the authentication fails. To resolve the issue of differing clock times, a Grace Period permits a wider window for CRL validity.",
        "type": "integer",
        "required": false
      },
      {
        "name": "grace-period-extension-for-secure-remote-secure-client",
        "description": "When dealing with remote clients the Grace Period needs to be extended. The remote client sometimes relies on the peer gateway to supply the CRL. If the client's clock is not synchronized with the gateway's clock, a CRL that is considered valid by the gateway may be considered invalid by the client.",
        "type": "integer",
        "required": false
      },
      {
        "name": "support-ike-dos-protection-from-identified-src",
        "description": "When the number of IKE negotiations handled simultaneously exceeds a threshold above VPN's capacity, a gateway concludes that it is either under a high load or experiencing a Denial of Service attack. VPN can filter out peers that are the probable source of the potential Denial of Service attack. There are two kinds of protection: Stateless - the peer has to respond to an IKE notification in a way that proves the peer's IP address is not spoofed. If the peer cannot prove this, VPN does not allocate resources for the IKE negotiation Puzzles - this is the same as Stateless, but in addition, the peer has to solve a mathematical puzzle. Solving this puzzle consumes peer CPU resources in a way that makes it difficult to initiate multiple IKE negotiations simultaneously.Puzzles is more secure then Stateless, but affects performance.Since these kinds of attacks involve a new proprietary addition to the IKE protocol, enabling these protection mechanisms may cause difficulties with non Check Point VPN products or older versions of VPN.",
        "type": "string",
        "required": false,
        "valid_values": [
          "puzzles",
          "stateless",
          "none"
        ]
      },
      {
        "name": "support-ike-dos-protection-from-unidentified-src",
        "description": "When the number of IKE negotiations handled simultaneously exceeds a threshold above VPN's capacity, a gateway concludes that it is either under a high load or experiencing a Denial of Service attack. VPN can filter out peers that are the probable source of the potential Denial of Service attack. There are two kinds of protection: Stateless - the peer has to respond to an IKE notification in a way that proves the peer's IP address is not spoofed. If the peer cannot prove this, VPN does not allocate resources for the IKE negotiation Puzzles - this is the same as Stateless, but in addition, the peer has to solve a mathematical puzzle. Solving this puzzle consumes peer CPU resources in a way that makes it difficult to initiate multiple IKE negotiations simultaneously.Puzzles is more secure then Stateless, but affects performance.Since these kinds of attacks involve a new proprietary addition to the IKE protocol, enabling these protection mechanisms may cause difficulties with non Check Point VPN products or older versions of VPN.",
        "type": "string",
        "required": false,
        "valid_values": [
          "puzzles",
          "stateless",
          "none"
        ]
      },
      {
        "name": "remote-access",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "allowonlysinglelogintouser",
          "allowseverallogintouser"
        ]
      },
      {
        "name": "enable-back-connections",
        "description": "Usually communication with remote clients must be initialized by the clients. However, once a client has opened a connection, the hosts behind VPN can open a return or back connection to the client. For a back connection, the client's details must be maintained on all the devices between the client and the gateway, and on the gateway itself. Determine whether the back connection is enabled.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "keep-alive-packet-to-gw-interval",
        "description": "Usually communication with remote clients must be initialized by the clients. However, once a client has opened a connection, the hosts behind VPN can open a return or back connection to the client. For a back connection, the client's details must be maintained on all the devices between the client and the gateway, and on the gateway itself. Determine frequency (in seconds) of the Keep Alive packets sent by the client in order to maintain the connection with the gateway.Available only if enable-back-connections is true.",
        "type": "integer",
        "required": false
      },
      {
        "name": "encrypt-dns-traffic",
        "description": "You can decide whether DNS queries sent by the remote client to a DNS server located on the corporate LAN are passed through the VPN tunnel or not. Disable this option if the client has to make DNS queries to the DNS server on the corporate LAN while connecting to the organization but without using the SecuRemote client.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "simultaneous-login-mode",
        "description": "Select the simultaneous login mode.",
        "type": "string",
        "required": false,
        "valid_values": [
          "allowonlysinglelogintouser",
          "allowseverallogintouser"
        ]
      },
      {
        "name": "vpn-authentication-and-encryption",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "AES-256",
          "DES",
          "AES-128",
          "3DES"
        ]
      },
      {
        "name": "encryption-algorithms",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "AES-256",
          "DES",
          "AES-128",
          "3DES"
        ]
      },
      {
        "name": "ike",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "AES-256",
          "DES",
          "AES-128",
          "3DES"
        ]
      },
      {
        "name": "support-encryption-algorithms",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "aes-128",
        "description": "Select whether the AES-128 encryption algorithm will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "aes-256",
        "description": "Select whether the AES-256 encryption algorithm will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "des",
        "description": "Select whether the DES encryption algorithm will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "tdes",
        "description": "Select whether the Triple DES encryption algorithm will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "use-encryption-algorithm",
        "description": "Choose the encryption algorithm that will have the highest priority of the selected algorithms. If given a choice of more that one encryption algorithm to use, the algorithm selected in this field will be used.",
        "type": "string",
        "required": false,
        "valid_values": [
          "AES-256",
          "DES",
          "AES-128",
          "3DES"
        ]
      },
      {
        "name": "support-data-integrity",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "aes-xcbc",
        "description": "Select whether the AES-XCBC hash algorithm will be supported with remote hosts to ensure data integrity.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "md5",
        "description": "Select whether the MD5 hash algorithm will be supported with remote hosts to ensure data integrity.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "sha1",
        "description": "Select whether the SHA1 hash algorithm will be supported with remote hosts to ensure data integrity.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "sha256",
        "description": "Select whether the SHA256 hash algorithm will be supported with remote hosts to ensure data integrity.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "sha384",
        "description": "Select whether the SHA384 hash algorithm will be supported with remote hosts to ensure data integrity.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "sha512",
        "description": "Select whether the SHA512 hash algorithm will be supported with remote hosts to ensure data integrity.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "use-data-integrity",
        "description": "The hash algorithm chosen here will be given the highest priority if more than one choice is offered.",
        "type": "string",
        "required": false,
        "valid_values": [
          "sha512",
          "sha384",
          "aes-xcbc",
          "sha256",
          "sha1",
          "md5"
        ]
      },
      {
        "name": "support-diffie-hellman-groups",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "group1",
        "description": "Select whether Diffie-Hellman Group 1 (768 bit) will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "group14",
        "description": "Select whether Diffie-Hellman Group 14 (2048 bit) will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "group15",
        "description": "Select whether Diffie-Hellman Group 15 (3072 bit) will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "group16",
        "description": "Select whether Diffie-Hellman Group 16 (4096 bit) will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "group17",
        "description": "Select whether Diffie-Hellman Group 17 (6144 bit) will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "group18",
        "description": "Select whether Diffie-Hellman Group 18 (8192 bit) will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "group19",
        "description": "Select whether Diffie-Hellman Group 19 (256-bit ECP) will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "group2",
        "description": "Select whether Diffie-Hellman Group 2 (1024 bit) will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "group20",
        "description": "Select whether Diffie-Hellman Group 20 (384-bit ECP) will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "group21",
        "description": "Select whether Diffie-Hellman Group 21 (521-bit ECP) will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "group5",
        "description": "Select whether Diffie-Hellman Group 5 (1536 bit) will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "use-diffie-hellman-group",
        "description": "SecureClient users utilize the Diffie-Hellman group selected in this field.",
        "type": "string",
        "required": false,
        "valid_values": [
          "group 1",
          "group 2",
          "group 5",
          "group 14",
          "group 15",
          "group 16",
          "group 17",
          "group 18",
          "group 19",
          "group 20",
          "group 21"
        ]
      },
      {
        "name": "ipsec",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "AES-256",
          "DES",
          "AES-128",
          "3DES"
        ]
      },
      {
        "name": "support-encryption-algorithms",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "aes-128",
        "description": "Select whether the AES-128 encryption algorithm will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "aes-256",
        "description": "Select whether the AES-256 encryption algorithm will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "des",
        "description": "Select whether the DES encryption algorithm will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "tdes",
        "description": "Select whether the Triple DES encryption algorithm will be supported with remote hosts.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "use-encryption-algorithm",
        "description": "Choose the encryption algorithm that will have the highest priority of the selected algorithms. If given a choice of more that one encryption algorithm to use, the algorithm selected in this field will be used.",
        "type": "string",
        "required": false,
        "valid_values": [
          "AES-256",
          "DES",
          "AES-128",
          "3DES"
        ]
      },
      {
        "name": "support-data-integrity",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "aes-xcbc",
        "description": "Select whether the AES-XCBC hash algorithm will be supported with remote hosts to ensure data integrity.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "md5",
        "description": "Select whether the MD5 hash algorithm will be supported with remote hosts to ensure data integrity.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "sha1",
        "description": "Select whether the SHA1 hash algorithm will be supported with remote hosts to ensure data integrity.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "sha256",
        "description": "Select whether the SHA256 hash algorithm will be supported with remote hosts to ensure data integrity.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "sha384",
        "description": "Select whether the SHA384 hash algorithm will be supported with remote hosts to ensure data integrity.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "sha512",
        "description": "Select whether the SHA512 hash algorithm will be supported with remote hosts to ensure data integrity.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "use-data-integrity",
        "description": "The hash algorithm chosen here will be given the highest priority if more than one choice is offered.",
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
        "name": "enforce-encryption-alg-and-data-integrity-on-all-users",
        "description": "Enforce Encryption Algorithm and Data Integrity on all users.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "encryption-method",
        "description": "Select the encryption method.",
        "type": "string",
        "required": false,
        "valid_values": [
          "prefer_ikev2_support_ikev1",
          "ike_v2_only",
          "ike_v1_only"
        ]
      },
      {
        "name": "pre-shared-secret",
        "description": "the user password is specified in the Authentication tab in the user's IKE properties (in the user properties window: Encryption tab > Edit).",
        "type": "boolean",
        "required": false
      },
      {
        "name": "support-legacy-auth-for-sc-l2tp-nokia-clients",
        "description": "Support Legacy Authentication for SC (hybrid mode), L2TP (PAP) and Nokia clients (CRACK).",
        "type": "boolean",
        "required": false
      },
      {
        "name": "support-legacy-eap",
        "description": "Support Legacy EAP (Extensible Authentication Protocol).",
        "type": "boolean",
        "required": false
      },
      {
        "name": "support-l2tp-with-pre-shared-key",
        "description": "Use a centrally managed pre-shared key for IKE.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "l2tp-pre-shared-key",
        "description": "Type in the pre-shared key.Available only if support-l2tp-with-pre-shared-key is set to true.",
        "type": "string",
        "required": false
      },
      {
        "name": "vpn-advanced",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "allow-clear-traffic-to-encryption-domain-when-disconnected",
        "description": "SecuRemote/SecureClient behavior while disconnected - How traffic to the VPN domain is handled when the Remote Access VPN client is not connected to the site. Traffic can either be dropped or sent in clear without encryption.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "enable-load-distribution-for-mep-conf",
        "description": "Load distribution for Multiple Entry Points configurations - Remote access clients will randomly select a gateway from the list of entry points. Make sure to define the same VPN domain for all the Security Gateways you want to be entry points.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "use-first-allocated-om-ip-addr-for-all-conn-to-the-gws-of-the-site",
        "description": "Use first allocated Office Mode IP Address for all connections to the Gateways of the site.After a remote user connects and receives an Office Mode IP address from a gateway, every connection to that gateways encryption domain will go out with the Office Mode IP as the internal source IP. The Office Mode IP is what hosts in the encryption domain will recognize as the remote user's IP address. The Office Mode IP address assigned by a specific gateway can be used in its own encryption domain and in neighboring encryption domains as well. The neighboring encryption domains should reside behind gateways that are members of the same VPN community as the assigning gateway. Since the remote hosts connections are dependant on the Office Mode IP address it received, should the gateway that issued the IP become unavailable, all the connections to the site will terminate.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "scv",
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
        "name": "apply-scv-on-simplified-mode-fw-policies",
        "description": "Determine whether the gateway verifies that remote access clients are securely configured. This is set here only if the security policy is defined in the Simplified Mode. If the security policy is defined in the Traditional Mode, verification takes place per rule.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "exceptions",
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
        "name": "hosts",
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
        "name": "services",
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
        "name": "no-scv-for-unsupported-cp-clients",
        "description": "Do not apply Secure Configuration Verification for connections from Check Point VPN clients that don't support it, such as SSL Network Extender, GO, Capsule VPN / Connect, Endpoint Connects lower than R75, or L2TP clients.Available only if apply-scv-on-simplified-mode-fw-policies is true.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "upon-verification-accept-and-log-client-connection",
        "description": "If the gateway verifies the client's configuration, decide how the gateway should handle connections with clients that fail the Security Configuration Verification. It is possible to either drop the connection or Accept the connection and log it.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "only-tcp-ip-protocols-are-used",
        "description": "Most SCV checks are configured via the SCV policy. Specify whether to verify that only TCP/IP protocols are used.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "policy-installed-on-all-interfaces",
        "description": "Most SCV checks are configured via the SCV policy. Specify whether to verify that the Desktop Security Policy is installed on all the interfaces of the client.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "generate-log",
        "description": "If the client identifies that the secure configuration has been violated, select whether a log is generated by the remote access client and sent to the Security Management server.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "notify-user",
        "description": "If the client identifies that the secure configuration has been violated, select whether to user should be notified.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "ssl-network-extender",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "certificate_with_enrollment",
          "certificate",
          "mixed",
          "legacy"
        ]
      },
      {
        "name": "user-auth-method",
        "description": "Wide Impact: Also applies for SecureClient Mobile devices and Check Point GO clients!User authentication method indicates how the user will be authenticated by the gateway. Changes made here will also apply for SSL clients.Legacy - Username and password only.Certificate - Certificate only with an existing certificate.Certificate with Enrollment - Allows you to obtain a new certificate and then use certificate authentication only.Mixed - Can use either username and password or certificate.",
        "type": "string",
        "required": false,
        "valid_values": [
          "certificate_with_enrollment",
          "certificate",
          "mixed",
          "legacy"
        ]
      },
      {
        "name": "supported-encryption-methods",
        "description": "Wide Impact: Also applies to SecureClient Mobile devices!Select the encryption algorithms that will be supported for remote users. Changes made here will also apply for all SSL clients.",
        "type": "string",
        "required": false,
        "valid_values": [
          "3des_or_rc4",
          "3des_only"
        ]
      },
      {
        "name": "client-upgrade-upon-connection",
        "description": "When a client connects to the gateway with SSL Network Extender, the client automatically checks for upgrade. Select whether the client should automatically upgrade.",
        "type": "string",
        "required": false,
        "valid_values": [
          "force_upgrade",
          "ask_user",
          "no_upgrade"
        ]
      },
      {
        "name": "client-uninstall-upon-disconnection",
        "description": "Select whether the client should automatically uninstall SSL Network Extender when it disconnects from the gateway.",
        "type": "string",
        "required": false,
        "valid_values": [
          "force_uninstall",
          "ask_user",
          "dont_uninstall"
        ]
      },
      {
        "name": "re-auth-user-interval",
        "description": "Wide Impact: Applies for the SecureClient Mobile!Select the interval that users will need to reauthenticate.",
        "type": "integer",
        "required": false
      },
      {
        "name": "scan-ep-machine-for-compliance-with-ep-compliance-policy",
        "description": "Set to true if you want endpoint machines to be scanned for compliance with the Endpoint Compliance Policy.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "client-outgoing-keep-alive-packets-frequency",
        "description": "Select the interval which the keep-alive packets are sent.",
        "type": "integer",
        "required": false
      },
      {
        "name": "secure-client-mobile",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "certificate_with_enrollment",
          "certificate",
          "mixed",
          "legacy"
        ]
      },
      {
        "name": "user-auth-method",
        "description": "Wide Impact: Also applies for SSL Network Extender clients and Check Point GO clients!How the user will be authenticated by the gateway.",
        "type": "string",
        "required": false,
        "valid_values": [
          "certificate_with_enrollment",
          "certificate",
          "mixed",
          "legacy"
        ]
      },
      {
        "name": "enable-password-caching",
        "description": "If the password entered to authenticate is saved locally on the user's machine.",
        "type": "string",
        "required": false,
        "valid_values": [
          "client_decide",
          "true",
          "false"
        ]
      },
      {
        "name": "cache-password-timeout",
        "description": "Cached password timeout (in minutes).",
        "type": "integer",
        "required": false
      },
      {
        "name": "re-auth-user-interval",
        "description": "Wide Impact: Also applies for SSL Network Extender clients!The length of time (in minutes) until the user's credentials are resent to the gateway to verify authorization.",
        "type": "integer",
        "required": false
      },
      {
        "name": "connect-mode",
        "description": "Methods by which a connection to the gateway will be initiated:Configured On Endpoint Client - the method used for initiating a connection to a gateway is determined by the endpoint clientManual - VPN connections will not be initiated automatically.Always connected - SecureClient Mobile will automatically establish a connection to the last connected gateway under the following circumstances: (a) the device has a valid IP address, (b) when the device \"wakes up\" from a low-power state or a soft-reset, or (c) after a condition that caused the device to automatically disconnect ceases to exist (for example, Device is out of PC Sync, Disconnect is not idle.).On application request - Applications requiring access to resources through the VPN will be able to initiate a VPN connection.",
        "type": "string",
        "required": false,
        "valid_values": [
          "manual",
          "always connected",
          "on application request",
          "configured on endpoint client"
        ]
      },
      {
        "name": "automatically-initiate-dialup",
        "description": "When selected, the client will initiate a GPRS dialup connection before attempting to establish the VPN connection. Note that if a local IP address is already available through another network interface, then the GPRS dialup is not initiated.",
        "type": "string",
        "required": false,
        "valid_values": [
          "client_decide",
          "true",
          "false"
        ]
      },
      {
        "name": "disconnect-when-device-is-idle",
        "description": "Enabling this feature will disconnect users from the gateway if there is no traffic sent during the defined time period.",
        "type": "string",
        "required": false,
        "valid_values": [
          "client_decide",
          "true",
          "false"
        ]
      },
      {
        "name": "supported-encryption-methods",
        "description": "Wide Impact: Also applies for SSL Network Extender clients!Select the encryption algorithms that will be supported with remote users.",
        "type": "string",
        "required": false,
        "valid_values": [
          "3des_or_rc4",
          "3des_only"
        ]
      },
      {
        "name": "route-all-traffic-to-gw",
        "description": "Operates the client in Hub Mode, sending all traffic to the VPN server for routing, filtering, and processing.",
        "type": "string",
        "required": false,
        "valid_values": [
          "client_decide",
          "true",
          "false"
        ]
      },
      {
        "name": "endpoint-connect",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "client_decide",
          "true",
          "false"
        ]
      },
      {
        "name": "enable-password-caching",
        "description": "If the password entered to authenticate is saved locally on the user's machine.",
        "type": "string",
        "required": false,
        "valid_values": [
          "client_decide",
          "true",
          "false"
        ]
      },
      {
        "name": "cache-password-timeout",
        "description": "Cached password timeout (in minutes).",
        "type": "integer",
        "required": false
      },
      {
        "name": "re-auth-user-interval",
        "description": "The length of time (in minutes) until the user's credentials are resent to the gateway to verify authorization.",
        "type": "integer",
        "required": false
      },
      {
        "name": "connect-mode",
        "description": "Methods by which a connection to the gateway will be initiated:Manual - VPN connections will not be initiated automatically.Always connected - Endpoint Connect will automatically establish a connection to the last connected gateway under the following circumstances: (a) the device has a valid IP address, (b) when the device \"wakes up\" from a low-power state or a soft-reset, or (c) after a condition that caused the device to automatically disconnect ceases to exist (for example, Device is out of PC Sync, Disconnect is not idle.).Configured on endpoint client - the method used for initiating a connection to a gateway is determined by the endpoint client.",
        "type": "string",
        "required": false,
        "valid_values": [
          "Manual",
          "Always Connected",
          "Configured On Endpoint Client"
        ]
      },
      {
        "name": "network-location-awareness",
        "description": "Wide Impact: Also applies for Check Point GO clients!Endpoint Connect intelligently detects whether it is inside or outside of the VPN domain (Enterprise LAN), and automatically connects or disconnects as required. Select true and edit network-location-awareness-conf to configure this capability.",
        "type": "string",
        "required": false,
        "valid_values": [
          "client_decide",
          "true",
          "false"
        ]
      },
      {
        "name": "network-location-awareness-conf",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "connects to gw through internal interface",
          "connects from network or group",
          "runs on computer with access to active directory domain"
        ]
      },
      {
        "name": "vpn-clients-are-considered-inside-the-internal-network-when-the-client",
        "description": "When a VPN client is within the internal network, the internal resources are available and the VPN tunnel should be disconnected. Determine when VPN clients are considered inside the internal network:Connects to GW through internal interface - The client connects to the gateway through one of its internal interfaces (recommended).Connects from network or group - The client connects from a network or group specified in network-or-group-of-conn-vpn-client.Runs on computer with access to Active Directory domain - The client runs on a computer that can access its Active Directory domain.Note: The VPN tunnel will resume automatically when the VPN client is no longer in the internal network and the client is set to \"Always connected\" mode.",
        "type": "string",
        "required": false,
        "valid_values": [
          "connects to gw through internal interface",
          "connects from network or group",
          "runs on computer with access to active directory domain"
        ]
      },
      {
        "name": "network-or-group-of-conn-vpn-client",
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
        "name": "consider-wireless-networks-as-external",
        "description": "The speed at which locations are classified as internal or external can be increased by creating a list of wireless networks that are known to be external. A wireless network is identified by its Service Set Identifier (SSID) a name used to identify a particular 802.11 wireless LAN.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "dns-suffixes",
        "description": "DNS suffixes not defined here will be considered as external. If this list is empty consider-undefined-dns-suffixes-as-external will automatically be set to false.Available only if consider-undefined-dns-suffixes-as-external is set to true.",
        "type": "array",
        "required": false
      },
      {
        "name": "excluded-internal-wireless-networks",
        "description": "Excludes the specified internal networks names (SSIDs).Available only if consider-wireless-networks-as-external is set to true.",
        "type": "array",
        "required": false
      },
      {
        "name": "consider-undefined-dns-suffixes-as-external",
        "description": "The speed at which locations are classified as internal or external can be increased by creating a list of DNS suffixes that are known to be external. Enable this to be able to define DNS suffixes which won't be considered external.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "remember-previously-detected-external-networks",
        "description": "The speed at which locations are classified as internal or external can be increased by caching (on the client side) names of networks that were previously determined to be external.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "disconnect-when-conn-to-network-is-lost",
        "description": "Enabling this feature disconnects users from the gateway when connectivity to the network is lost.",
        "type": "string",
        "required": false,
        "valid_values": [
          "client_decide",
          "true",
          "false"
        ]
      },
      {
        "name": "disconnect-when-device-is-idle",
        "description": "Enabling this feature will disconnect users from the gateway if there is no traffic sent during the defined time period.",
        "type": "string",
        "required": false,
        "valid_values": [
          "client_decide",
          "true",
          "false"
        ]
      },
      {
        "name": "route-all-traffic-to-gw",
        "description": "Operates the client in Hub Mode, sending all traffic to the VPN server for routing, filtering, and processing.",
        "type": "string",
        "required": false,
        "valid_values": [
          "client_decide",
          "true",
          "false"
        ]
      },
      {
        "name": "client-upgrade-mode",
        "description": "Select an option to determine how the client is upgraded.",
        "type": "string",
        "required": false,
        "valid_values": [
          "force_upgrade",
          "ask_user",
          "no_upgrade"
        ]
      },
      {
        "name": "hot-spot-and-hotel-registration",
        "description": "",
        "type": "array",
        "required": false
      },
      {
        "name": "enable-registration",
        "description": "Set Enable registration to true in order to configure settings. Set Enable registration to false in order to cancel registration (the configurations below won't be available). When the feature is enabled, you have several minutes to complete registration.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "local-subnets-access-only",
        "description": "Local subnets access only.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "registration-timeout",
        "description": "Maximum time (in seconds) to complete registration.",
        "type": "integer",
        "required": false
      },
      {
        "name": "track-log",
        "description": "Track log.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "max-ip-access-during-registration",
        "description": "Maximum number of addresses to allow access to during registration.",
        "type": "integer",
        "required": false
      },
      {
        "name": "ports",
        "description": "Ports to be opened during registration (up to 10 ports).",
        "type": "array",
        "required": false
      },
      {
        "name": "user-directory",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "no display",
          "display upon request",
          "display"
        ]
      },
      {
        "name": "enable-password-change-when-user-active-directory-expires",
        "description": "For organizations using MS Active Directory, this setting enables users whose passwords have expired to automatically create new passwords.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "cache-size",
        "description": "The maximum number of cached users allowed. The cache is FIFO (first-in, first-out). When a new user is added to a full cache, the first user is deleted to make room for the new user. The Check Point Security Gateway does not query the LDAP server for users already in the cache, unless the cache has timed out.",
        "type": "integer",
        "required": false
      },
      {
        "name": "enable-password-expiration-configuration",
        "description": "Enable configuring of the number of days during which the password is valid.If enable-password-change-when-user-active-directory-expires is true, the password expiration time is determined by the Active Directory. In this case it is recommended not to set this to true.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "password-expires-after",
        "description": "Specifies the number of days during which the password is valid. Users are authenticated using a special LDAP password. Should this password expire, a new password must be defined.Available only if enable-password-expiration-configuration is true.",
        "type": "integer",
        "required": false
      },
      {
        "name": "timeout-on-cached-users",
        "description": "The period of time in which a cached user is timed out and will need to be fetched again from the LDAP server.",
        "type": "integer",
        "required": false
      },
      {
        "name": "display-user-dn-at-login",
        "description": "Decide whether or not you would like to display the user's DN when logging in. If you choose to display the user DN, you can select whether to display it, when the user is prompted for the password at login, or on the request of the authentication scheme. This property is a useful diagnostic tool when there is more than one user with the same name in an Account Unit. In this case, the first one is chosen and the others are ignored.",
        "type": "string",
        "required": false,
        "valid_values": [
          "no display",
          "display upon request",
          "display"
        ]
      },
      {
        "name": "enforce-rules-for-user-mgmt-admins",
        "description": "Enforces password strength rules on LDAP users when you create or modify a Check Point Password.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "min-password-length",
        "description": "Specifies the minimum length (in characters) of the password.",
        "type": "integer",
        "required": false
      },
      {
        "name": "password-must-include-a-digit",
        "description": "Password must include a digit.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "password-must-include-a-symbol",
        "description": "Password must include a symbol.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "password-must-include-lowercase-char",
        "description": "Password must include a lowercase character.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "password-must-include-uppercase-char",
        "description": "Password must include an uppercase character.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "qos",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "bits-per-sec",
          "bytes-per-sec",
          "kbits-per-sec",
          "kbytes-per-sec",
          "mbits-per-sec",
          "mbytes-per-sec"
        ]
      },
      {
        "name": "default-weight-of-rule",
        "description": "Define a Weight at which bandwidth will be guaranteed. Set a default weight for a rule.Note: Value will be applied to new rules only.",
        "type": "integer",
        "required": false
      },
      {
        "name": "max-weight-of-rule",
        "description": "Define a Weight at which bandwidth will be guaranteed. Set a maximum weight for a rule.",
        "type": "integer",
        "required": false
      },
      {
        "name": "unit-of-measure",
        "description": "Define the Rate at which packets are transmitted, for which bandwidth will be guaranteed. Set a Unit of measure.",
        "type": "string",
        "required": false,
        "valid_values": [
          "bits-per-sec",
          "bytes-per-sec",
          "kbits-per-sec",
          "kbytes-per-sec",
          "mbits-per-sec",
          "mbytes-per-sec"
        ]
      },
      {
        "name": "authenticated-ip-expiration",
        "description": "Define the Authentication time-out for QoS. This timeout is set in minutes. In an Authenticated IP all connections which are open in a specified time limit will be guaranteed bandwidth, but will not be guaranteed bandwidth after the time limit.",
        "type": "integer",
        "required": false
      },
      {
        "name": "non-authenticated-ip-expiration",
        "description": "Define the Authentication time-out for QoS. This timeout is set in minutes.",
        "type": "integer",
        "required": false
      },
      {
        "name": "unanswered-queried-ip-expiration",
        "description": "Define the Authentication time-out for QoS. This timeout is set in minutes.",
        "type": "integer",
        "required": false
      },
      {
        "name": "carrier-security",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "before last",
          "last"
        ]
      },
      {
        "name": "block-gtp-in-gtp",
        "description": "Prevents GTP packets from being encapsulated inside GTP tunnels. When this option is checked, such packets are dropped and logged.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "enforce-gtp-anti-spoofing",
        "description": "verifies that G-PDUs are using the end user IP address that has been agreed upon in the PDP context activation process. When this option is checked, packets that do not use this IP address are dropped and logged.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "produce-extended-logs-on-unmatched-pdus",
        "description": "logs GTP packets not matched by previous rules with Carrier Security's extended GTP-related log fields. These logs are brown and their Action attribute is empty. The default setting is checked.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "produce-extended-logs-on-unmatched-pdus-position",
        "description": "Choose to place this implicit rule Before Last or as the Last rule.Available only if produce-extended-logs-on-unmatched-pdus is true.",
        "type": "string",
        "required": false,
        "valid_values": [
          "before last",
          "last"
        ]
      },
      {
        "name": "protocol-violation-track-option",
        "description": "Set the appropriate track or alert option to be used when a protocol violation (malformed packet) is detected.",
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
        "name": "enable-g-pdu-seq-number-check-with-max-deviation",
        "description": "If set to false, sequence checking is not enforced and all out-of-sequence G-PDUs will be accepted.To enhance performance, disable this extended integrity test.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "g-pdu-seq-number-check-max-deviation",
        "description": "specifies that a G-PDU is accepted only if the difference between its sequence number and the expected sequence number is less than or equal to the allowed deviation.Available only ifenable-g-pdu-seq-number-check-with-max-deviation is true.",
        "type": "integer",
        "required": false
      },
      {
        "name": "verify-flow-labels",
        "description": "See that each packet's flow label matches the flow labels defined by GTP signaling. This option is relevant for GTP version 0 only.To enhance performance, disable this extended integrity test.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "allow-ggsn-replies-from-multiple-interfaces",
        "description": "Allows GTP signaling replies from an IP address different from the IP address to which the requests are sent (Relevant only for gateways below R80).",
        "type": "boolean",
        "required": false
      },
      {
        "name": "enable-reverse-connections",
        "description": "Allows Carrier Security gateways to accept PDUs sent from the GGSN to the SGSN, on a previously established PDP context, even if these PDUs are sent over ports that do not match the ports of the established PDP context.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "gtp-signaling-rate-limit-sampling-interval",
        "description": "Works in correlation with the property Enforce GTP Signal packet rate limit found in the Carrier Security window of the GSN network object. For example, with the rate limit sampling interval default of 1 second, and the network object enforced a GTP signal packet rate limit of the default 2048 PDU per second, sampling will occur one time per second, or 2048 signaling PDUs between two consecutive samplings.",
        "type": "integer",
        "required": false
      },
      {
        "name": "one-gtp-echo-on-each-path-frequency",
        "description": "sets the number of GTP Echo exchanges per path allowed per configured time period. Echo requests exceeding this rate are dropped and logged. Setting the value to 0 disables the feature and allows an unlimited number of echo requests per path at any interval.",
        "type": "integer",
        "required": false
      },
      {
        "name": "aggressive-aging",
        "description": "If true, enables configuring aggressive aging thresholds and time out value.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "aggressive-timeout",
        "description": "Aggressive timeout. Available only if aggressive-aging is true.",
        "type": "integer",
        "required": false
      },
      {
        "name": "memory-activation-threshold",
        "description": "Memory activation threshold. Available only if aggressive-aging is true.",
        "type": "integer",
        "required": false
      },
      {
        "name": "memory-deactivation-threshold",
        "description": "Memory deactivation threshold. Available only if aggressive-aging is true.",
        "type": "integer",
        "required": false
      },
      {
        "name": "tunnel-activation-threshold",
        "description": "Tunnel activation threshold. Available only if aggressive-aging is true.",
        "type": "integer",
        "required": false
      },
      {
        "name": "tunnel-deactivation-threshold",
        "description": "Tunnel deactivation threshold. Available only if aggressive-aging is true.",
        "type": "integer",
        "required": false
      },
      {
        "name": "user-accounts",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "expire after",
          "expire at"
        ]
      },
      {
        "name": "expiration-date-method",
        "description": "Select an Expiration Date Method.Expire at - Account expires on the date that you select.Expire after - Account expires after the number of days that you select.",
        "type": "string",
        "required": false,
        "valid_values": [
          "expire after",
          "expire at"
        ]
      },
      {
        "name": "expiration-date",
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
        "name": "days-until-expiration",
        "description": "Account expires after the number of days that you select.",
        "type": "integer",
        "required": false
      },
      {
        "name": "show-accounts-expiration-indication-days-in-advance",
        "description": "Activates the Expired Accounts link, to open the Expired Accounts window.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "days-in-advance-to-show-accounts-expiration-indication",
        "description": "Days in advance to show accounts expiration indication.",
        "type": "integer",
        "required": false
      },
      {
        "name": "user-authority",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "selectively",
          "all"
        ]
      },
      {
        "name": "display-web-access-view",
        "description": "Specify whether or not to display the WebAccess rule base. This rule base is used for UserAuthority.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "windows-domains-to-trust",
        "description": "When matching Firewall usernames to Windows Domains usernames for Single Sign on, selectwhether to trust all or specify which Windows Domain should be trusted.ALL - Enables you to allow all Windows domains to access the internal sites of the organization.SELECTIVELY - Enables you to specify which Windows domains will have access to the internal sites of the organization.",
        "type": "string",
        "required": false,
        "valid_values": [
          "selectively",
          "all"
        ]
      },
      {
        "name": "trust-only-following-windows-domains",
        "description": "Specify which Windows domains will have access to the internal sites of the organization.Available only if windows-domains-to-trust is set to SELECTIVELY.",
        "type": "array",
        "required": false
      },
      {
        "name": "connect-control",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "load-agents-port",
        "description": "Sets the port number on which load measuring agents communicate with ConnectControl.",
        "type": "integer",
        "required": false
      },
      {
        "name": "load-measurement-interval",
        "description": "sets how often (in seconds) the load measuring agents report their load status to ConnectControl.",
        "type": "integer",
        "required": false
      },
      {
        "name": "persistence-server-timeout",
        "description": "Sets the amount of time (in seconds) that a client, once directed to a particular server, will continue to be directed to that same server.",
        "type": "integer",
        "required": false
      },
      {
        "name": "server-availability-check-interval",
        "description": "Sets how often (in seconds) ConnectControl checks to make sure the load balanced servers are running and responding to service requests.",
        "type": "integer",
        "required": false
      },
      {
        "name": "server-check-retries",
        "description": "Sets how many times ConnectControl attempts to contact a server before ceasing to direct traffic to it.",
        "type": "integer",
        "required": false
      },
      {
        "name": "stateful-inspection",
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
        "name": "tcp-start-timeout",
        "description": "A TCP connection will be timed out if the interval between the arrival of the first packet and establishment of the connection (TCP three-way handshake) exceeds TCP start timeout seconds.",
        "type": "integer",
        "required": false
      },
      {
        "name": "tcp-session-timeout",
        "description": "The length of time (in seconds) an idle connection will remain in the Security Gateway connections table.",
        "type": "integer",
        "required": false
      },
      {
        "name": "tcp-end-timeout",
        "description": "A TCP connection will only terminate TCP end timeout seconds after two FIN packets (one in each direction: client-to-server, and server-to-client) or an RST packet. When a TCP connection ends (FIN packets sent or connection reset) the Check Point Security Gateway will keep the connection in the connections table for another TCP end timeout seconds, to allow for stray ACKs of the connection that arrive late.",
        "type": "integer",
        "required": false
      },
      {
        "name": "tcp-end-timeout-r8020-gw-and-above",
        "description": "A TCP connection will only terminate TCP end timeout seconds after two FIN packets (one in each direction: client-to-server, and server-to-client) or an RST packet. When a TCP connection ends (FIN packets sent or connection reset) the Check Point Security Gateway will keep the connection in the connections table for another TCP end timeout seconds, to allow for stray ACKs of the connection that arrive late.",
        "type": "integer",
        "required": false
      },
      {
        "name": "udp-virtual-session-timeout",
        "description": "Specifies the amount of time (in seconds) a UDP reply channel may remain open without any packets being returned.",
        "type": "integer",
        "required": false
      },
      {
        "name": "icmp-virtual-session-timeout",
        "description": "An ICMP virtual session will be considered to have timed out after this time period (in seconds).",
        "type": "integer",
        "required": false
      },
      {
        "name": "other-ip-protocols-virtual-session-timeout",
        "description": "A virtual session of services which are not explicitly configured here will be considered to have timed out after this time period (in seconds).",
        "type": "integer",
        "required": false
      },
      {
        "name": "sctp-start-timeout",
        "description": "SCTP connections will be timed out if the interval between the arrival of the first packet and establishment of the connection exceeds this value (in seconds).",
        "type": "integer",
        "required": false
      },
      {
        "name": "sctp-session-timeout",
        "description": "Time (in seconds) an idle connection will remain in the Security Gateway connections table.",
        "type": "integer",
        "required": false
      },
      {
        "name": "sctp-end-timeout",
        "description": "SCTP connections end after this number of seconds, after the connection ends or is reset, to allow for stray ACKs of the connection that arrive late.",
        "type": "integer",
        "required": false
      },
      {
        "name": "accept-stateful-udp-replies-for-unknown-services",
        "description": "Specifies if UDP replies are to be accepted for unknown services.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "accept-stateful-icmp-errors",
        "description": "Accept ICMP error packets which refer to another non-ICMP connection (for example, to an ongoing TCP or UDP connection) that was accepted by the Rule Base.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "accept-stateful-icmp-replies",
        "description": "Accept ICMP reply packets for ICMP requests that were accepted by the Rule Base.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "accept-stateful-other-ip-protocols-replies-for-unknown-services",
        "description": "Accept reply packets for other undefined services (that is, services which are not one of the following: TCP, UDP, ICMP).",
        "type": "boolean",
        "required": false
      },
      {
        "name": "drop-out-of-state-tcp-packets",
        "description": "Drop TCP packets which are not consistent with the current state of the connection.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "log-on-drop-out-of-state-tcp-packets",
        "description": "Generates a log entry when these out of state TCP packets are dropped.Available only if drop-out-of-state-tcp-packets is true.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "tcp-out-of-state-drop-exceptions",
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
        "name": "drop-out-of-state-icmp-packets",
        "description": "Drop ICMP packets which are not consistent with the current state of the connection.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "log-on-drop-out-of-state-icmp-packets",
        "description": "Generates a log entry when these out of state ICMP packets are dropped.Available only if drop-out-of-state-icmp-packets is true.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "drop-out-of-state-sctp-packets",
        "description": "Drop SCTP packets which are not consistent with the current state of the connection.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "log-on-drop-out-of-state-sctp-packets",
        "description": "Generates a log entry when these out of state SCTP packets are dropped.Available only if drop-out-of-state-sctp-packets is true.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "log-and-alert",
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
        "name": "administrative-notifications",
        "description": "Administrative notifications specifies the action to be taken when an administrative event (for example, when a certificate is about to expire) occurs.",
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
        "name": "connection-matched-by-sam",
        "description": "Connection matched by SAM specifies the action to be taken when a connection is blocked by SAM (Suspicious Activities Monitoring).",
        "type": "string",
        "required": false,
        "valid_values": [
          "Popup Alert",
          "Mail Alert",
          "SNMP Trap Alert",
          "User Defined Alert no.1",
          "User Defined Alert no.2",
          "User Defined Alert no.3"
        ]
      },
      {
        "name": "dynamic-object-resolution-failure",
        "description": "Dynamic object resolution failure specifies the action to be taken when a dynamic object cannot be resolved.",
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
        "name": "ip-options-drop",
        "description": "IP Options drop specifies the action to take when a packet with IP Options is encountered. The Check Point Security Gateway always drops these packets, but you can log them or issue an alert.",
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
        "name": "packet-is-incorrectly-tagged",
        "description": "Packet is incorrectly tagged.",
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
        "name": "packet-tagging-brute-force-attack",
        "description": "Packet tagging brute force attack.",
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
        "name": "sla-violation",
        "description": "SLA violation specifies the action to be taken when an SLA violation occurs, as defined in the Virtual Links window.",
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
        "name": "vpn-conf-and-key-exchange-errors",
        "description": "VPN configuration & key exchange errors specifies the action to be taken when logging configuration or key exchange errors occur, for example, when attempting to establish encrypted communication with a network object inside the same encryption domain.",
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
        "name": "vpn-packet-handling-error",
        "description": "VPN packet handling errors specifies the action to be taken when encryption or decryption errors occurs. A log entry contains the action performed (Drop or Reject) and a short description of the error cause, for example, scheme or method mismatch.",
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
        "name": "vpn-successful-key-exchange",
        "description": "VPN successful key exchange specifies the action to be taken when VPN keys are successfully exchanged.",
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
        "name": "log-every-authenticated-http-connection",
        "description": "Log every authenticated HTTP connection specifies that a log entry should be generated for every authenticated HTTP connection.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "log-traffic",
        "description": "Log Traffic specifies whether or not to log traffic.",
        "type": "string",
        "required": false,
        "valid_values": [
          "none",
          "log"
        ]
      },
      {
        "name": "alerts",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "Popup Alert",
          "Mail Alert",
          "SNMP Trap Alert",
          "User Defined Alert no.1",
          "User Defined Alert no.2",
          "User Defined Alert no.3"
        ]
      },
      {
        "name": "send-popup-alert-to-smartview-monitor",
        "description": "Send popup alert to SmartView Monitor when an alert is issued, it is also sent to SmartView Monitor.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "popup-alert-script",
        "description": "Run popup alert script the operating system script to be executed when an alert is issued. For example, set another form of notification, such as an email or a user-defined command.",
        "type": "string",
        "required": false
      },
      {
        "name": "send-mail-alert-to-smartview-monitor",
        "description": "Send mail alert to SmartView Monitor when a mail alert is issued, it is also sent to SmartView Monitor.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "mail-alert-script",
        "description": "Run mail alert script the operating system script to be executed when Mail is specified as the Track in a rule. The default is internal_sendmail, which is not a script but an internal Security Gateway command.",
        "type": "string",
        "required": false
      },
      {
        "name": "send-snmp-trap-alert-to-smartview-monitor",
        "description": "Send SNMP trap alert to SmartView Monitor when an SNMP trap alert is issued, it is also sent to SmartView Monitor.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "snmp-trap-alert-script",
        "description": "Run SNMP trap alert script command to be executed when SNMP Trap is specified as the Track in a rule. By default the internal_snmp_trap is used. This command is executed by the fwd process.",
        "type": "string",
        "required": false
      },
      {
        "name": "send-user-defined-alert-num1-to-smartview-monitor",
        "description": "Send user defined alert no. 1 to SmartView Monitor when an alert is issued, it is also sent to SmartView Monitor.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "user-defined-script-num1",
        "description": "Run user defined script the operating system script to be run when User-Defined is specified as the Track in a rule, or when User Defined Alert no. 1 is selected as a Track Option.",
        "type": "string",
        "required": false
      },
      {
        "name": "send-user-defined-alert-num2-to-smartview-monitor",
        "description": "Send user defined alert no. 2 to SmartView Monitor when an alert is issued, it is also sent to SmartView Monitor.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "user-defined-script-num2",
        "description": "Run user defined 2 script the operating system script to be run when User-Defined is specified as the Track in a rule, or when User Defined Alert no. 2 is selected as a Track Option.",
        "type": "string",
        "required": false
      },
      {
        "name": "send-user-defined-alert-num3-to-smartview-monitor",
        "description": "Send user defined alert no. 3 to SmartView Monitor when an alert is issued, it is also sent to SmartView Monitor.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "user-defined-script-num3",
        "description": "Run user defined 3 script the operating system script to be run when User-Defined is specified as the Track in a rule, or when User Defined Alert no. 3 is selected as a Track Option.",
        "type": "string",
        "required": false
      },
      {
        "name": "default-track-option-for-system-alerts",
        "description": "Set the default track option for System Alerts.",
        "type": "string",
        "required": false,
        "valid_values": [
          "Popup Alert",
          "Mail Alert",
          "SNMP Trap Alert",
          "User Defined Alert no.1",
          "User Defined Alert no.2",
          "User Defined Alert no.3"
        ]
      },
      {
        "name": "time-settings",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "excessive-log-grace-period",
        "description": "Specifies the minimum amount of time (in seconds) between consecutive logs of similar packets. Two packets are considered similar if they have the same source address, source port, destination address, and destination port; and the same protocol was used. After the first packet, similar packets encountered in the grace period will be acted upon according to the security policy, but only the first packet generates a log entry or an alert. Any value from 0 to 90 seconds can be entered in this field.Note: This option only applies for DROP rules with logging.",
        "type": "integer",
        "required": false
      },
      {
        "name": "logs-resolving-timeout",
        "description": "Specifies the amount of time (in seconds), after which the log page is displayed without resolving names and while showing only IP addresses. Any value from 0 to 90 seconds can be entered in this field.",
        "type": "integer",
        "required": false
      },
      {
        "name": "status-fetching-interval",
        "description": "Specifies the frequency at which the Security Management server queries the Check Point Security gateway, Check Point QoS and other gateways it manages for status information. Any value from 30 to 900 seconds can be entered in this field.",
        "type": "integer",
        "required": false
      },
      {
        "name": "virtual-link-statistics-logging-interval",
        "description": "Specifies the frequency (in seconds) with which Virtual Link statistics will be logged. This parameter is relevant only for Virtual Links defined with SmartView Monitor statistics enabled in the SLA Parameters tab of the Virtual Link window. Any value from 60 to 3600 seconds can be entered in this field.",
        "type": "integer",
        "required": false
      },
      {
        "name": "data-access-control",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "auto-download-important-data",
        "description": "Automatically download and install Software Blade Contracts, security updates and other important data (highly recommended).",
        "type": "boolean",
        "required": false
      },
      {
        "name": "auto-download-sw-updates-and-new-features",
        "description": "Automatically download software updates and new features (highly recommended).Available only if auto-download-important-data is set to true.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "send-anonymous-info",
        "description": "Help Check Point improve the product by sending anonymous information.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "share-sensitive-info",
        "description": "Approve sharing core dump files and other relevant crash data which might contain personal information. All shared data will be processed in accordance with Check Point's Privacy Policy.Available only if send-anonymous-info is set to true.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "non-unique-ip-address-ranges",
        "description": "",
        "type": "array",
        "required": false,
        "valid_values": [
          "IPv4",
          "IPv6"
        ]
      },
      {
        "name": "address-type",
        "description": "The type of the IP Address.",
        "type": "string",
        "required": false,
        "valid_values": [
          "IPv4",
          "IPv6"
        ]
      },
      {
        "name": "first-ipv4-address",
        "description": "The first IPV4 Address in the range.",
        "type": "string",
        "required": false
      },
      {
        "name": "first-ipv6-address",
        "description": "The first IPV6 Address in the range.",
        "type": "string",
        "required": false
      },
      {
        "name": "last-ipv4-address",
        "description": "The last IPV4 Address in the range.",
        "type": "string",
        "required": false
      },
      {
        "name": "last-ipv6-address",
        "description": "The last IPV6 Address in the range.",
        "type": "string",
        "required": false
      },
      {
        "name": "proxy",
        "description": "",
        "type": "Object",
        "required": false
      },
      {
        "name": "use-proxy-server",
        "description": "If set to true, a proxy server is used when features need to access the internet.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "proxy-address",
        "description": "Specify the URL or IP address of the proxy server.Available only if use-proxy-server is set to true.",
        "type": "string",
        "required": false
      },
      {
        "name": "proxy-port",
        "description": "Specify the Port on which the server will be accessed.Available only if use-proxy-server is set to true.",
        "type": "integer",
        "required": false
      },
      {
        "name": "user-check",
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
        "name": "preferred-language",
        "description": "The preferred language for new UserCheck message.",
        "type": "string",
        "required": false
      },
      {
        "name": "send-emails-using-mail-server",
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
        "name": "hit-count",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "3 months",
          "6 months",
          "1 year",
          "2 years"
        ]
      },
      {
        "name": "enable-hit-count",
        "description": "Select to enable or clear to disable all Security Gateways to monitor the number of connections each rule matches.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "keep-hit-count-data-up-to",
        "description": "Select one of the time range options. Data is kept in the Security Management Server database for this period and is shown in the Hits column.",
        "type": "string",
        "required": false,
        "valid_values": [
          "3 months",
          "6 months",
          "1 year",
          "2 years"
        ]
      },
      {
        "name": "advanced-conf",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "off",
          "alert",
          "fail"
        ]
      },
      {
        "name": "certs-and-pki",
        "description": "",
        "type": "Object",
        "required": false,
        "valid_values": [
          "off",
          "alert",
          "fail"
        ]
      },
      {
        "name": "cert-validation-enforce-key-size",
        "description": "Enforce key length in certificate validation (R80+ gateways only).",
        "type": "string",
        "required": false,
        "valid_values": [
          "off",
          "alert",
          "fail"
        ]
      },
      {
        "name": "host-certs-ecdsa-key-size",
        "description": "Select the key size for ECDSA of the host certificate.",
        "type": "string",
        "required": false,
        "valid_values": [
          "p-256",
          "p-384",
          "p-521"
        ]
      },
      {
        "name": "host-certs-key-size",
        "description": "Select the key size of the host certificate.",
        "type": "string",
        "required": false,
        "valid_values": [
          "4096",
          "1024",
          "2048",
          "3072"
        ]
      },
      {
        "name": "keep-ike-sas",
        "description": "Enabled: Keep ALL IKEv1 phase 1 Security Associations (SA) upon policy installation.Disabled: Delete ALL IKEv1 phase 1 Security Associations (SA) upon policy installation.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "allow-remote-registration-of-opsec-products",
        "description": "After installing an OPSEC application, the remote administration (RA) utility enables an OPSEC product to finish registering itself without having to access the SmartConsole. If set to true, any host including the application host can run the utility. Otherwise, the RA utility can only be run from the Security Management host.",
        "type": "boolean",
        "required": false
      },
      {
        "name": "num-spoofing-errs-that-trigger-brute-force",
        "description": "Indicates how many incorrectly signed packets will be tolerated before assuming that there is an attack on the packet tagging and revoking the client's key.",
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
    "set-global-properties with a new added HTTP Server": {
      "description": "",
      "request": "POST {{server}}/set-global-properties\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"firewall\" : {\n    \"security-server\" : {\n      \"http-servers\" : {\n        \"add\" : {\n          \"logical-name\" : \"unique logical name\",\n          \"host\" : \"host name of server\",\n          \"port\" : 8080,\n          \"reauthentication\" : \"post request\"\n        }\n      }\n    }\n  }\n}",
      "response": ""
    },
    "set-global-properties with encryption algorithms": {
      "description": "",
      "request": "POST {{server}}/set-global-properties\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"remote-access\" : {\n    \"vpn-authentication-and-encryption\" : {\n      \"encryption-algorithms\" : {\n        \"ipsec\" : {\n          \"support-encryption-algorithms\" : {\n            \"tdes\" : true,\n            \"aes-256\" : true\n          },\n          \"use-encryption-algorithm\" : \"aes-256\"\n        }\n      }\n    }\n  }\n}",
      "response": ""
    },
    "set-global-properties with Identity Awareness": {
      "description": "",
      "request": "POST {{server}}/set-global-properties\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"identity-awareness\" : {\n    \"cache-mode\" : true,\n    \"cache-mode-duration\" : 99\n  }\n}",
      "response": ""
    },
    "set-global-properties with Network Location Awareness configurations": {
      "description": "",
      "request": "POST {{server}}/set-global-properties\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"remote-access\" : {\n    \"endpoint-connect\" : {\n      \"network-location-awareness\" : true,\n      \"network-location-awareness-conf\" : {\n        \"vpn-clients-are-considered-inside-the-internal-network-when-the-client\" : \"connects from network or group\",\n        \"network-or-group-of-conn-vpn-client\" : \"someNetwork\",\n        \"consider-wireless-networks-as-external\" : true,\n        \"excluded-internal-wireless-networks\" : {\n          \"add\" : \"wirelessNetworkName\"\n        },\n        \"consider-undefined-dns-suffixes-as-external\" : true,\n        \"dns-suffixes\" : {\n          \"add\" : \"aSuffix.com\"\n        }\n      }\n    }\n  }\n}",
      "response": ""
    },
    "set-global-properties with Non Unique IP Addresses": {
      "description": "",
      "request": "POST {{server}}/set-global-properties\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"non-unique-ip-address-ranges\" : {\n    \"add\" : [ {\n      \"address-type\" : \"ipv4\",\n      \"first-ipv4-address\" : \"1.2.3.4\",\n      \"last-ipv4-address\" : \"5.6.7.8\"\n    }, {\n      \"address-type\" : \"ipv6\",\n      \"first-ipv6-address\" : \"2001:db8:85a3::8a2e:370:7334\",\n      \"last-ipv6-address\" : \"2001:db8:85a3::8a2e:370:7335\"\n    } ]\n  }\n}",
      "response": ""
    },
    "set-global-properties with SCV exceptions": {
      "description": "Specify hosts that can be accessed using the selected services even if the client is not verified",
      "request": "POST {{server}}/set-global-properties\nContent-Type: application/json\nX-chkp-sid: {{session}}\n\n{\n  \"remote-access\" : {\n    \"scv\" : {\n      \"apply-scv-on-simplified-mode-fw-policies\" : true,\n      \"exceptions\" : {\n        \"add\" : {\n          \"hosts\" : [ \"host1\", \"host2\" ],\n          \"services\" : \"AH\"\n        }\n      }\n    }\n  }\n}",
      "response": ""
    }
  },
  "metadata": {
    "version": "2.0.1",
    "extracted_at": "2025-10-05T21:36:17.162875",
    "source_file": "set-global-properties.html"
  }
}
```