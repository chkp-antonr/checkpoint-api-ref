# show-best-practice with the "show-regulations" parameter

**Collection:** Web API (version 2.1) > 69 Best Practice
**Method:** `POST`
**URL:** `{{server}}/v2.1/show-best-practice`

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "best-practice-id": "VPN136",
  "show-regulations": true
}
```

## Example Responses

### Example 1: show-best-practice with the "show-regulations" parameter
**Status:** `200 OK`

**Body:**
```javascript
{
  "uid": "ae7b90c2-739d-4c31-86e3-022588e9e754",
  "name": "Check the Authentication Method defined in the IPSec VPN blade",
  "type": "compliance-best-practice",
  "domain": {
    "uid": "41e821a0-3720-11e3-aa6e-0800200c9fde",
    "name": "SMC User",
    "domain-type": "domain"
  },
  "meta-info": {
    "lock": "unlocked",
    "validation-state": "ok",
    "last-modify-time": {
      "posix": 1747861267880,
      "iso-8601": "2025-05-22T00:01+0300"
    },
    "last-modifier": "System",
    "creation-time": {
      "posix": 1747665909812,
      "iso-8601": "2025-05-19T17:45+0300"
    },
    "creator": "System"
  },
  "available-actions": {
    "edit": "true",
    "delete": "true",
    "clone": "true"
  },
  "read-only": false,
  "best-practice-id": "VPN136",
  "description": "This checks the Authentication settings for IPSec VPN on each relevant Security Gateway. These settings are configured in the Security Gateway object - 'VPN Clients' section - 'Authentication' page. The Authentication Method should be set to 'SecurID' or 'Personal Certificate'. If 'Defined On User Record (Legacy)' is selected, this Security Check examines the enabled Authentication Schemes in the 'Other' section - 'Legacy Authentication' page. These options should be cleared: 'Check Point Password', 'OS Password'.",
  "action-item": "In the Security Gateway object, expand the 'VPN Clients' section > click the 'Authentication' page. In the section 'Allow older clients to connect to this gateway', click 'Settings' and select either 'SecurID' or 'Personal Certificate'. If you select 'Defined On User Record (Legacy)', then in the 'Other' section > 'Legacy Authentication' page, you must clear these options: 'Check Point Password', 'OS Password'. Install the Access Control Policy.",
  "status": "poor",
  "blade": "ipsec-vpn",
  "user-defined": false,
  "relevant-objects": {
    "relevant-objects-type": "cpm-relevant-object",
    "cpm-relevant-objects-info": [
      {
        "uid": "0651ac0c-a25c-441f-a156-54d983516e1b",
        "name": "gw1",
        "status": "poor",
        "enabled": true,
        "relevant-object-type": "simple-gateway"
      }
    ]
  },
  "active": true,
  "regulations": [
    {
      "requirement-uid": "036f0e8f-db4d-459b-86ba-f8ef57aeb8aa",
      "requirement-id": "CIP-005-5: Req. 1.5",
      "requirement-description": "Have one or more methods for detecting known or suspected malicious communications for both inbound and outbound communications. [Taken from Requirement 5: Cyber Security - Electronic Security Perimeter(s)]",
      "requirement-status": "Medium",
      "regulation-name": "NERC CIP (v.5)"
    },
    {
      "requirement-uid": "b3d2a731-10c2-430d-9c0b-fda6ea8f741e",
      "requirement-id": "I 501.0 - 2",
      "requirement-description": "All users are identified and authenticated. [Katakri Base level requirement (IV): Security of Information Systems, subdivision I 500, Question I 501.0: Are the users identified and authenticated before access is granted to the information network and information systems of the organisation?]",
      "requirement-status": "Poor",
      "regulation-name": "Katakri 3.0"
    },
    {
      "requirement-uid": "2b0cd69e-aa76-4db0-839e-6663f32538d3",
      "requirement-id": "190055",
      "requirement-description": "4.1: Use strong cryptography and security protocols (for example, SSL/TLS, IPSEC, SSH, etc.) to safeguard sensitive cardholder data during transmission over open, public networks, including the following: 1) Only trusted keys and certificates are accepted. 2) The protocol in use only supports secure versions or configurations. 3) The encryption strength is appropriate for the encryption methodology in use. [Original PCI DSS 3.0 Reference: 4.1]",
      "requirement-status": "Good",
      "regulation-name": "PCI DSS 3.0"
    },
    {
      "requirement-uid": "1c587581-2695-490c-b763-5ef2fd674a67",
      "requirement-id": "CIP-007-5: Req. 5.1",
      "requirement-description": "Have a method(s) to enforce authentication of interactive user access, where technically feasible. [Taken from Requirement 7: Cyber Security - System Security Management]",
      "requirement-status": "Medium",
      "regulation-name": "NERC CIP (v.5)"
    },
    {
      "requirement-uid": "84e74cfe-f84c-40c8-afd4-de5ed3ecfc21",
      "requirement-id": "I 501.0 - 4",
      "requirement-description": "Identification and authentication is done by using well known and secure techniques or it is otherwise taken care on a secure manner. [Katakri Base level requirement (IV): Security of Information Systems, subdivision I 500, Question I 501.0: Are the users identified and authenticated before access is granted to the information network and information systems of the organisation?]",
      "requirement-status": "Medium",
      "regulation-name": "Katakri 3.0"
    },
    {
      "requirement-uid": "bd26086d-61c6-42ed-810d-6554f06041bd",
      "requirement-id": "010082",
      "requirement-description": "User authentication for external connections - Appropriate authentication methods shall be used to control access by remote users. [Original ISO 27001 Reference: 11.4.2]",
      "requirement-status": "Medium",
      "regulation-name": "ISO 27001"
    },
    {
      "requirement-uid": "ce1827a8-14fe-4d5d-8b3f-e3ca8bf19946",
      "requirement-id": "010053",
      "requirement-description": "Network controls - Networks shall be adequately managed and controlled, in order to be protected from threats, and to maintain security for the systems and applications using the network, including information in transit. [Original ISO 27001 Reference: 10.6.1]",
      "requirement-status": "Good",
      "regulation-name": "ISO 27001"
    },
    {
      "requirement-uid": "db535b52-c17c-453f-8b0e-d2804b2a0699",
      "requirement-id": "010097",
      "requirement-description": "Teleworking - A policy, operational plans and procedures shall be developed and implemented for teleworking activities. [Original ISO 27001 Reference: 11.7.2]",
      "requirement-status": "Poor",
      "regulation-name": "ISO 27001"
    },
    {
      "requirement-uid": "2ff36a5c-87bd-4bdc-9f06-ea7b56022675",
      "requirement-id": "010131",
      "requirement-description": "Technical compliance checking - Information systems shall be regularly checked for compliance with security implementation standards. [Original ISO 27001 Reference: 15.2.2]",
      "requirement-status": "Good",
      "regulation-name": "ISO 27001"
    },
    {
      "requirement-uid": "6b3e9f11-a9fa-421b-9726-fa905c557ae8",
      "requirement-id": "030021",
      "requirement-description": "Develop configuration standards for all system components. Assure that these standards address all known security vulnerabilities and are consistent with industry-accepted system hardening standards [Original PCI DSS 2.0 Reference: Requirement 2: Do not use vendor-supplied defaults for system passwords and other security parameters: 2.2]",
      "requirement-status": "Good",
      "regulation-name": "PCI DSS 2.0"
    },
    {
      "requirement-uid": "2ea05494-ab9b-40b4-b663-dd31ecfbc6d3",
      "requirement-id": "030024",
      "requirement-description": "Configure system security parameters to prevent misuse [Original PCI DSS 2.0 Reference: Requirement 2: Do not use vendor-supplied defaults for system passwords and other security parameters: 2.2.3]",
      "requirement-status": "Good",
      "regulation-name": "PCI DSS 2.0"
    },
    {
      "requirement-uid": "40ad1e9a-8900-42ee-a849-1947401b00f1",
      "requirement-id": "030085",
      "requirement-description": "In addition to assigning a unique ID, employ at least one of the following methods to authenticate all users: a) Something you know, such as a password or passphrase, b) Something you have, such as a token device or smart card, c) Something you are, such as a biometric [Original PCI DSS 2.0 Reference: Requirement 8: Assign a unique ID to each person with computer access: 8.2]",
      "requirement-status": "Poor",
      "regulation-name": "PCI DSS 2.0"
    },
    {
      "requirement-uid": "186318ae-85a2-405c-a34c-21ca8917882c",
      "requirement-id": "030086",
      "requirement-description": "Incorporate two-factor authentication for remote access (network-level access originating from outside the network) to the network by employees, administrators, and third parties [Original PCI DSS 2.0 Reference: Requirement 8: Assign a unique ID to each person with computer access: 8.3]",
      "requirement-status": "Poor",
      "regulation-name": "PCI DSS 2.0"
    },
    {
      "requirement-uid": "afaa2a03-e834-43de-a1bd-220280846578",
      "requirement-id": "020002",
      "requirement-description": "Risk Management  - Implement security measures sufficient to reduce risks and vulnerabilities to a reasonable and appropriate level to comply with Section 164.306(a). [Original HIPAA Reference: Administrative Safeguards: 164.308 (a)(1)(ii)(B)]",
      "requirement-status": "Good",
      "regulation-name": "HIPAA Security"
    },
    {
      "requirement-uid": "8ce50f01-78cc-41aa-917c-06521d5ff7d6",
      "requirement-id": "020046",
      "requirement-description": "Policies and Procedures - Implement reasonable and appropriate policies and procedures to comply with the standards, implementation specifications, or other requirements of this subpart, taking into account those factors specified in 164.306(b)(2)(i), (ii), (iii), and (iv).  [Original HIPAA Reference: Policies and Procedures: 164.316 (a)]",
      "requirement-status": "Good",
      "regulation-name": "HIPAA Security"
    },
    {
      "requirement-uid": "69c72261-047e-4cb2-bf5d-97a393b66252",
      "requirement-id": "030026",
      "requirement-description": "Encrypt all non-console administrative access using strong cryptography. Use technologies such as SSH, VPN, or SSL/TLS for web-based management and other non-console administrative access [Original PCI DSS 2.0 Reference: Requirement 2: Do not use vendor-supplied defaults for system passwords and other security parameters: 2.3]",
      "requirement-status": "Good",
      "regulation-name": "PCI DSS 2.0"
    },
    {
      "requirement-uid": "b68993aa-2bca-4200-adfa-46a1b09a6201",
      "requirement-id": "050003",
      "requirement-description": "In furtherance of the policy in subsection (a), each agency or authority described in section 505(a) shall establish appropriate standards for the financial institutions subject to their jurisdiction relating to administrative, technical, and physical safeguards to protect against any anticipated threats or hazards to the security or integrity of such records [Original GLBA Reference: Title V - Privacy, Subtitle A - Disclosure of Nonpublic Personal Information, Sec. 501 Protection of nonpublic personal information, (b.2) Financial Institutions Safeguard]",
      "requirement-status": "Good",
      "regulation-name": "GLBA"
    },
    {
      "requirement-uid": "5e6bda76-d47e-418a-9783-ee3b2af0079d",
      "requirement-id": "050004",
      "requirement-description": "In furtherance of the policy in subsection (a), each agency or authority described in section 505(a) shall establish appropriate standards for the financial institutions subject to their jurisdiction relating to administrative, technical, and physical safeguards to protect against unauthorized access to or use of such records or information which could result in substantial harm or inconvenience to any customer. [Original GLBA Reference: Title V - Privacy, Subtitle A - Disclosure of Nonpublic Personal Information, Sec. 501 Protection of nonpublic personal information, (b.3) Financial Institutions Safeguard]",
      "requirement-status": "Good",
      "regulation-name": "GLBA"
    },
    {
      "requirement-uid": "1c335b4d-4602-43bf-a8f0-df1a20952cfb",
      "requirement-id": "020040",
      "requirement-description": "Person or Entity Authentication - Implement procedures to verify that a person or entity seeking access to electronic protected health information is the one claimed. [Original HIPAA Reference: Technical Safeguards: 164.312 (d)]",
      "requirement-status": "Poor",
      "regulation-name": "HIPAA Security"
    },
    {
      "requirement-uid": "f3f4c576-d0e7-4cc9-8667-12c285674632",
      "requirement-id": "050002",
      "requirement-description": "In furtherance of the policy in subsection (a), each agency or authority described in section 505(a) shall establish appropriate standards for the financial institutions subject to their jurisdiction relating to administrative, technical, and physical safeguards to insure the security and confidentiality of customer records and information [Original GLBA Reference: Title V - Privacy, Subtitle A - Disclosure of Nonpublic Personal Information, Sec. 501 Protection of nonpublic personal information, (b.1) Financial Institutions Safeguard]",
      "requirement-status": "Good",
      "regulation-name": "GLBA"
    },
    {
      "requirement-uid": "c9c47405-600d-4946-a6b8-8d6f4df7d80d",
      "requirement-id": "070031",
      "requirement-description": "Network managers should implement controls to ensure the security of information in networks, and the protection of connected services from unauthorized access. In particular, the following items should be considered: e) management activities should be closely co-ordinated both to optimize the service to the organization and to ensure that controls are consistently applied across the information processing infrastructure. [Original ISO 27002 Reference: 10.6.1-5]",
      "requirement-status": "Good",
      "regulation-name": "ISO 27002"
    },
    {
      "requirement-uid": "e14cbf11-113c-4f89-9ceb-7c58f1a4062a",
      "requirement-id": "070030",
      "requirement-description": "Network managers should implement controls to ensure the security of information in networks, and the protection of connected services from unauthorized access. In particular, the following items should be considered: d) appropriate logging and monitoring should be applied to enable recording of security relevant actions. [Original ISO 27002 Reference: 10.6.1-4]",
      "requirement-status": "Good",
      "regulation-name": "ISO 27002"
    },
    {
      "requirement-uid": "95e4f73c-6437-4ee0-a908-3cec37fa2d83",
      "requirement-id": "070028",
      "requirement-description": "Network managers should implement controls to ensure the security of information in networks, and the protection of connected services from unauthorized access. In particular, the following items should be considered: b) responsibilities and procedures for the management of remote equipment, including equipment in user areas, should be established. [Original ISO 27002 Reference: 10.6.1-2]",
      "requirement-status": "Good",
      "regulation-name": "ISO 27002"
    },
    {
      "requirement-uid": "3bdc2f3a-4b1c-449c-aedf-c5cc790665c9",
      "requirement-id": "070206",
      "requirement-description": "The guidelines and arrangements to be considered should include the provision of suitable communication equipment, including methods for securing remote access. [Original ISO 27002 Reference: 11.7.2-13]",
      "requirement-status": "Good",
      "regulation-name": "ISO 27002"
    },
    {
      "requirement-uid": "ad0d0b10-09b0-4a14-9b3f-994c671cef60",
      "requirement-id": "070286",
      "requirement-description": "Technical compliance checking involves the examination of operational systems to ensure that hardware and software controls have been correctly implemented. This type of compliance checking requires specialist technical expertise. Compliance checking also covers, for example, penetration testing and vulnerability assessments, which might be carried out by independent experts specifically contracted for this purpose. This can be useful in detecting vulnerabilities in the system and for checking how effective the controls are in preventing unauthorized access due to these vulnerabilities.  Penetration testing and vulnerability assessments provide a snapshot of a system in a specific state at a specific time. The snapshot is limited to those portions of the system actually tested during the penetration attempt(s). Penetration testing and vulnerability assessments are not a substitute for risk assessment. [Original ISO 27002 Reference: 15.2.2-1]",
      "requirement-status": "Good",
      "regulation-name": "ISO 27002"
    },
    {
      "requirement-uid": "b77a1eb7-8336-4ad3-bd7f-b277a886224b",
      "requirement-id": "070027",
      "requirement-description": "Network managers should implement controls to ensure the security of information in networks, and the protection of connected services from unauthorized access. In particular, the following items should be considered: a) operational responsibility for networks should be separated from computer operations where appropriate. [Original ISO 27002 Reference: 10.6.1-1]",
      "requirement-status": "Good",
      "regulation-name": "ISO 27002"
    },
    {
      "requirement-uid": "3858605a-1da8-42fd-9703-9f47fddc8f70",
      "requirement-id": "070029",
      "requirement-description": "Network managers should implement controls to ensure the security of information in networks, and the protection of connected services from unauthorized access. In particular, the following items should be considered: c) special controls should be established to safeguard the confidentiality and integrity of data passing over public networks or over wireless networks, and to protect the connected systems and applications; special controls may also be required to maintain the availability of the network services and computers connected. [Original ISO 27002 Reference: 10.6.1-3]",
      "requirement-status": "Good",
      "regulation-name": "ISO 27002"
    },
    {
      "requirement-uid": "461129f6-f84d-4478-b4a7-9e8aa2e91e20",
      "requirement-id": "070149",
      "requirement-description": "Node authentication can serve as an alternative means of authenticating groups of remote users where they are connected to a secure, shared computer facility. Cryptographic techniques, e.g. based on machine certificates, can be used for node authentication. This is part of several VPN based solutions. [Original ISO 27002 Reference: 11.4.2-3]",
      "requirement-status": "Medium",
      "regulation-name": "ISO 27002"
    },
    {
      "requirement-uid": "93fcf355-e239-43e0-97e7-10e41a87c545",
      "requirement-id": "070197",
      "requirement-description": "Suitable protection of the teleworking site should be in place against, e.g., the theft of equipment and information, the unauthorized disclosure of information, unauthorized remote access to the organization's internal systems or misuse of facilities. Teleworking activities should both be authorized and controlled by management, and it should be ensured that suitable arrangements are in place for this way of working. The following matters should be considered: c) the communications security requirements, taking into account the need for remote access to the organization's internal systems, the sensitivity of the information that will be accessed and pass over the communication link and the sensitivity of the internal system. [Original ISO 27002 Reference: 11.7.2-4]",
      "requirement-status": "Poor",
      "regulation-name": "ISO 27002"
    },
    {
      "requirement-uid": "8e0f3cea-a40e-4753-a60b-6cfa06b868dd",
      "requirement-id": "070150",
      "requirement-description": "Additional authentication controls should be implemented to control access to wireless networks. In particular, special care is needed in the selection of controls for wireless networks due to the greater opportunities for undetected interception and insertion of network traffic. [Original ISO 27002 Reference: 11.4.2-4]",
      "requirement-status": "Medium",
      "regulation-name": "ISO 27002"
    },
    {
      "requirement-uid": "cf0a980d-32e9-45de-a260-e986966ace74",
      "requirement-id": "080074",
      "requirement-description": "Cryptographic Module Authentication - The information system uses mechanisms for authentication to a cryptographic module that meet the requirements of applicable federal laws, Executive Orders, directives, policies, regulations, standards, and guidance for such authentication. [Original NIST 800:53 Reference: Identification And Authentication: IA-7]",
      "requirement-status": "Good",
      "regulation-name": "NIST 800-53"
    },
    {
      "requirement-uid": "2b432a5a-8c52-458a-a9ec-91ab3a8ad6a3",
      "requirement-id": "080169",
      "requirement-description": "Trusted Path - The information system establishes a trusted communications path between the user and the following security functions of the system: [Assignment: organization-defined security functions to include at a minimum, information system authentication and reauthentication].  [Original NIST 800:53 Reference: System And Communications Protection: SC-11]",
      "requirement-status": "Poor",
      "regulation-name": "NIST 800-53"
    },
    {
      "requirement-uid": "47d4b84b-7842-47aa-94eb-8f941267f937",
      "requirement-id": "070174",
      "requirement-description": "Where strong authentication and identity verification is required, authentication methods alternative to passwords, such as cryptographic means, smart cards, tokens or biometric means, should be used. [Original ISO 27002 Reference: 11.5.2-5]",
      "requirement-status": "Poor",
      "regulation-name": "ISO 27002"
    },
    {
      "requirement-uid": "8d51ecbc-285e-4110-b1f1-eddaaa92fbf2",
      "requirement-id": "070194",
      "requirement-description": "Organizations should only authorize teleworking activities if they are satisfied that appropriate security arrangements and controls are in place, and that these comply with the organization's security policy. [Original ISO 27002 Reference: 11.7.2-1]",
      "requirement-status": "Poor",
      "regulation-name": "ISO 27002"
    },
    {
      "requirement-uid": "ff8b84f8-9050-4e17-bae0-9256d7fedc07",
      "requirement-id": "090007",
      "requirement-description": "Translate the overall IT security plan into enterprise information security baselines for all major platforms and integrate it into the configuration baseline. [Original CobiT 4.1 Reference: Deliver and Support / Ensure Systems Security / IT Security Plan: DS.5.2.1.3]",
      "requirement-status": "Good",
      "regulation-name": "CobiT 4.1"
    },
    {
      "requirement-uid": "c8a0de8f-e12c-41bd-8e8c-bf7cea8e83cd",
      "requirement-id": "070148",
      "requirement-description": "Dial-back procedures and controls, e.g. using dial-back modems, can provide protection against unauthorized and unwanted connections to an organization's information processing facilities. This type of control authenticates users trying to establish a connection to an organization's network from remote locations. When using this control, an organization should not use network services, which include call forwarding, or, if they do, they should disable the use of such features to avoid weaknesses associated with call forwarding. The call back process should ensure that an actual disconnection on the organization's side occurs. Otherwise, the remote user could hold the line open pretending that the call back verification has occurred. Call back procedures and controls should be thoroughly tested for this possibility. [Original ISO 27002 Reference: 11.4.2-2]",
      "requirement-status": "Medium",
      "regulation-name": "ISO 27002"
    },
    {
      "requirement-uid": "dc431028-9eb8-4151-b806-832144e8e362",
      "requirement-id": "080017",
      "requirement-description": "Remote Access - The organization: a. Documents allowed methods of remote access to the information system; b. Establishes usage restrictions and implementation guidance for each allowed remote access method; c. Monitors for unauthorized remote access to the information system; d. Authorizes remote access to the information system prior to connection; and e. Enforces requirements for remote connections to the information system. [Original NIST 800:53 Reference: Access Control: AC-17]",
      "requirement-status": "Medium",
      "regulation-name": "NIST 800-53"
    },
    {
      "requirement-uid": "009a109a-3feb-4323-b538-889c9c8be1dc",
      "requirement-id": "090012",
      "requirement-description": "Establish a method for authenticating and authorising users to establish responsibility and enforce access rights in line with sensitivity of information and functional application requirements and infrastructure components, and in compliance with applicable laws, regulations, internal policies and contractual agreements. [Original CobiT 4.1 Reference: Deliver and Support / Ensure Systems Security / Identity Management : DS.5.3.1.3]",
      "requirement-status": "Good",
      "regulation-name": "CobiT 4.1"
    },
    {
      "requirement-uid": "2f5f5d90-d7d9-42a3-b9a3-32c3cefbcf13",
      "requirement-id": "080019",
      "requirement-description": "Access Control For Mobile Devices - The organization: a. Establishes usage restrictions and implementation guidance for organization-controlled mobile devices; b. Authorizes connection of mobile devices meeting organizational usage restrictions and implementation guidance to organizational information systems; c. Monitors for unauthorized connections of mobile devices to organizational information systems; d. Enforces requirements for the connection of mobile devices to organizational information systems; e. Disables information system functionality that provides the capability for automatic execution of code on mobile devices without user direction; f. Issues specially configured mobile devices to individuals traveling to locations that the organization deems to be of significant risk in accordance with organizational policies and procedures; and g. Applies [Assignment: organization-defined inspection and preventative measures] to mobile devices returning from locations that the organization deems to be of significant risk in accordance with organizational policies and procedures. [Original NIST 800:53 Reference: Access Control: AC-19]",
      "requirement-status": "Medium",
      "regulation-name": "NIST 800-53"
    },
    {
      "requirement-uid": "dcdcd1fa-857c-4ba3-a336-0e74767fbf91",
      "requirement-id": "070147",
      "requirement-description": "Authentication of remote users can be achieved using, for example, a cryptographic based technique, hardware tokens, or a challenge/response protocol. Possible implementations of such techniques can be found in various virtual private network (VPN) solutions. Dedicated private lines can also be used to provide assurance of the source of connections. [Original ISO 27002 Reference: 11.4.2-1]",
      "requirement-status": "Medium",
      "regulation-name": "ISO 27002"
    },
    {
      "requirement-uid": "e36fae94-011f-4199-9235-0f16582bf4b2",
      "requirement-id": "110002",
      "requirement-description": "The network element must be password protected. [Original Firewall STIG Reference: VUL-ID: V-3012, Group Title: Network element is not password protected, Rule ID: SV-3012r2_rule, STIG-IG: NET0230, Severity: CAT I]",
      "requirement-status": "Good",
      "regulation-name": "Firewall STIG"
    },
    {
      "requirement-uid": "5c333d98-db59-41e6-83d4-2912377c8cff",
      "requirement-id": "140037",
      "requirement-description": "Outsourcing in any configuration or at any location should not result in any weakening or degradation of the FI's internal controls. The FI should require the service provider to employ a high standard of care and diligence in its security policies, procedures and controls to protect the confidentiality and security of its sensitive information, such as customer data, computer files, records, object programs and source codes. [Original MAS Reference: TRM 5.1.5: Management of IT Outsourcing Risks - Due Diligence]",
      "requirement-status": "Good",
      "regulation-name": "MAS TRM"
    },
    {
      "requirement-uid": "fe3970cb-2117-4687-b806-420d501a36c2",
      "requirement-id": "130011",
      "requirement-description": "Information Protection -The Responsible Entity shall implement and document a program to identify, classify, and protect information associated with Critical Cyber Assets. R4.1. The Critical Cyber Asset information to be protected shall include, at a minimum and regardless of media type, operational procedures, lists as required in Standard CIP-002-4, network topology or similar diagrams, floor plans of computing centers that contain Critical Cyber Assets, equipment layouts of Critical Cyber Assets, disaster recovery plans, incident response plans, and security configuration information. R4.2. The Responsible Entity shall classify information to be protected under this program based on the sensitivity of the Critical Cyber Asset information. R4.3. The Responsible Entity shall, at least annually, assess adherence to its Critical Cyber Asset information protection program, document the assessment results, and implement an action plan to remediate deficiencies identified during the assessment. [Original NERC Reference: Cyber Security - Security Management Controls: CIP-003-4 - R4]",
      "requirement-status": "Poor",
      "regulation-name": "NERC CIP"
    },
    {
      "requirement-uid": "3c4f5bb2-e14c-4b37-927b-0adbe2066d3e",
      "requirement-id": "110048",
      "requirement-description": "The network device must require authentication prior to establishing a management connection for administrative access. [Original Firewall STIG Reference: VUL-ID: V-3175, Group Title: Management connections must require passwords, Rule ID: SV-3175r3_rule, STIG-IG: NET1636, Severity: CAT I]",
      "requirement-status": "Good",
      "regulation-name": "Firewall STIG"
    },
    {
      "requirement-uid": "ad76588e-dc2f-4ffc-9d03-5079d5e14dbb",
      "requirement-id": "110050",
      "requirement-description": "The network element must only allow management connections for administrative access using FIPS 140-2 validated encryption algorithms or protocols. [Original Firewall STIG Reference: VUL-ID: V-3069, Group Title: Management connections must be secured by FIPS 140-2, Rule ID: SV-3069r2_rule, STIG-IG: NET1638, Severity: CAT II]",
      "requirement-status": "Good",
      "regulation-name": "Firewall STIG"
    },
    {
      "requirement-uid": "20738e7b-7d5d-493c-9a5a-d83408207d55",
      "requirement-id": "110020",
      "requirement-description": "The network element must use two or more authentication servers for the purpose of granting administrative access. [Original Firewall STIG Reference: VUL-ID: V-15432, Group Title: The device is not authenticated using a AAA server, Rule ID: SV-16259r2_rule, STIG-IG: NET0433, Severity: CAT II]",
      "requirement-status": "Good",
      "regulation-name": "Firewall STIG"
    },
    {
      "requirement-uid": "c6d3a81e-584c-4309-9209-cef859f8e347",
      "requirement-id": "140173",
      "requirement-description": "Information processed, stored or transmitted between an FI and its customers should be accurate, reliable and complete. With internet connection to internal networks, financial systems and devices may now be potentially accessed by anyone from anywhere at any time. The FI should implement physical and logical access security to allow only authorised personnel to access its systems. Appropriate processing and transmission controls should also be implemented to protect the integrity of systems and data. [Original MAS Reference: TRM 12.1.4: Online Financial Services - Online Systems Security]",
      "requirement-status": "Poor",
      "regulation-name": "MAS TRM"
    },
    {
      "requirement-uid": "4d996472-cb62-4848-bf88-a253d4de06ff",
      "requirement-id": "140176",
      "requirement-description": "FIs should implement two-factor authentication at login for all types of online financial systems and for authorising transactions. The primary objectives of two-factor authentication are to protect the confidentiality of customer account data and transaction details as well as enhance confidence in online systems by combating phishing, keylogging, spyware, malware, middleman attacks and other internet-based scams and malevolent exploits targeted at FIs and their customers. [Original MAS Reference: TRM 12.1.7: Online Financial Services - Online Systems Security]",
      "requirement-status": "Poor",
      "regulation-name": "MAS TRM"
    },
    {
      "requirement-uid": "497189f4-cefd-4e59-b93f-6634f304436c",
      "requirement-id": "150007",
      "requirement-description": "Translate the overall IT security plan into enterprise information security baselines for all major platforms and integrate it into the configuration baseline. [Original CobiT 4.1 Reference: Deliver and Support / Ensure Systems Security / IT Security Plan: DS.5.2.1.3]",
      "requirement-status": "Good",
      "regulation-name": "SOX"
    },
    {
      "requirement-uid": "2c35786c-edf0-41be-a572-0cac3704c955",
      "requirement-id": "140066",
      "requirement-description": "User access and data protection controls, at minimum, should be implemented in these applications. [Original MAS Reference: TRM 6.4.2: Acquisition and Development of Information Systems - End User Development]",
      "requirement-status": "Medium",
      "regulation-name": "MAS TRM"
    },
    {
      "requirement-uid": "3c493e69-f276-422e-bad6-f912fea4d593",
      "requirement-id": "160017",
      "requirement-description": "Remote Access - The organization: a. Documents allowed methods of remote access to the information system; b. Establishes usage restrictions and implementation guidance for each allowed remote access method; c. Monitors for unauthorized remote access to the information system; d. Authorizes remote access to the information system prior to connection; and e. Enforces requirements for remote connections to the information system. [Original NIST 800:53 Reference: Access Control: AC-17]",
      "requirement-status": "Medium",
      "regulation-name": "FIPS 200"
    },
    {
      "requirement-uid": "59b10691-6fdd-43a7-aac7-cd2ea2238d1e",
      "requirement-id": "160019",
      "requirement-description": "Access Control For Mobile Devices - The organization: a. Establishes usage restrictions and implementation guidance for organization-controlled mobile devices; b. Authorizes connection of mobile devices meeting organizational usage restrictions and implementation guidance to organizational information systems; c. Monitors for unauthorized connections of mobile devices to organizational information systems; d. Enforces requirements for the connection of mobile devices to organizational information systems; e. Disables information system functionality that provides the capability for automatic execution of code on mobile devices without user direction; f. Issues specially configured mobile devices to individuals traveling to locations that the organization deems to be of significant risk in accordance with organizational policies and procedures; and g. Applies [Assignment: organization-defined inspection and preventative measures] to mobile devices returning from locations that the organization deems to be of significant risk in accordance with organizational policies and procedures. [Original NIST 800:53 Reference: Access Control: AC-19]",
      "requirement-status": "Medium",
      "regulation-name": "FIPS 200"
    },
    {
      "requirement-uid": "342d8398-715e-4ca7-9beb-7841ffd0e09b",
      "requirement-id": "150012",
      "requirement-description": "Establish a method for authenticating and authorising users to establish responsibility and enforce access rights in line with sensitivity of information and functional application requirements and infrastructure components, and in compliance with applicable laws, regulations, internal policies and contractual agreements. [Original CobiT 4.1 Reference: Deliver and Support / Ensure Systems Security / Identity Management : DS.5.3.1.3]",
      "requirement-status": "Good",
      "regulation-name": "SOX"
    },
    {
      "requirement-uid": "4ec17b47-cdb5-4ac7-b704-4db8bf86054d",
      "requirement-id": "140181",
      "requirement-description": "Mobile online services and payment are extensions of the online financial services and payments services which are offered by FIs and accessible from the internet via computers or laptops. Security measures which are similar to those of online financial and payment systems should also be implemented on the mobile online services and payment systems. A risk assessment should be conducted to identify possible fraud scenarios and appropriate measures should be established to counteract payment card fraud via mobile devices. [Original MAS Reference: TRM 12.2.3: Online Financial Services - Mobile Online Services and Payments Security]",
      "requirement-status": "Poor",
      "regulation-name": "MAS TRM"
    },
    {
      "requirement-uid": "0e4c9407-cdfc-4a36-9b40-8a0f98b74f21",
      "requirement-id": "140169",
      "requirement-description": "Personnel with elevated system access entitlements should be closely supervised with all their systems activities logged and reviewed as they have the knowledge and resources to circumvent systems controls and security procedures. The following control and security practices should be adopted: a) Implement two-factor authentication for privileged users; b) Institute strong controls over remote access by privileged users; c) Restrict the number of privileged users; d) Grant privileged access on a 'need-to-have' basis; e) Maintain audit logging of system activities performed by privileged users; f) Disallow privileged users from accessing systems logs in which their activities are being captured; g) Review privileged users' activities on a timely basis; h) Prohibit sharing of privileged IDs and their access codes; i) Disallow vendors and contractors from gaining privileged access to systems without close supervision and monitoring; and j) Protect backup data from unauthorised access. [Original MAS Reference: TRM 11.2.3: Access Control - Privileged Access Management]",
      "requirement-status": "Medium",
      "regulation-name": "MAS TRM"
    },
    {
      "requirement-uid": "a07e6e03-f691-4725-ab46-846c083256a2",
      "requirement-id": "140170",
      "requirement-description": "More attacks will be targeted at FIs' internet systems as more financial services are being provided via the internet and more customers transacting on this platform. As a counter-measure, a security strategy should be devised and a suite of measures should be instituted to ensure the confidentiality, integrity and availability of data and systems. [Original MAS Reference: TRM 12.1.1: Online Financial Services - Online Systems Security]",
      "requirement-status": "Good",
      "regulation-name": "MAS TRM"
    },
    {
      "requirement-uid": "00d5ba31-b4da-4879-af0b-3e61bbded6f6",
      "requirement-id": "160074",
      "requirement-description": "Cryptographic Module Authentication - The information system uses mechanisms for authentication to a cryptographic module that meet the requirements of applicable federal laws, Executive Orders, directives, policies, regulations, standards, and guidance for such authentication. [Original NIST 800:53 Reference: Identification And Authentication: IA-7]",
      "requirement-status": "Good",
      "regulation-name": "FIPS 200"
    },
    {
      "requirement-uid": "2e25949a-042f-4309-8d75-c16f05b0b208",
      "requirement-id": "160169",
      "requirement-description": "Trusted Path - The information system establishes a trusted communications path between the user and the following security functions of the system: [Assignment: organization-defined security functions to include at a minimum, information system authentication and reauthentication].  [Original NIST 800:53 Reference: System And Communications Protection: SC-11]",
      "requirement-status": "Poor",
      "regulation-name": "FIPS 200"
    },
    {
      "requirement-uid": "c25ac033-7440-4b93-a9e5-074e80fad4a2",
      "requirement-id": "200097",
      "requirement-description": "5.6.2.2 Advanced Authentication - Advanced Authentication (AA) provides for additional security to the typical user identification and authentication of login ID and password, such as: biometric systems, user-based public key infrastructure (PKI), smart cards, software tokens, hardware tokens, paper (inert) tokens, or 'Risk-based Authentication' that includes a software token element comprised of a number of factors, such as network information, user information, positive device identification (i.e. device forensics, user pattern analysis and user binding), user profiling, and high-risk challenge/response questions. [Original CJIS Reference - Policy Area 6: Identification and Authentication]",
      "requirement-status": "Poor",
      "regulation-name": "CJIS"
    },
    {
      "requirement-uid": "522fc2cb-353c-4981-bf42-fdec79e14685",
      "requirement-id": "200050",
      "requirement-description": "5.5.6 Remote Access - The agency shall authorize, monitor, and control all methods of remote access to the information system. Remote access is any temporary access to an agency's information system by a user (or an information system) communicating temporarily through an external, non-agency-controlled network (e.g., the Internet). The agency shall employ automated mechanisms to facilitate the monitoring and control of remote access methods. The agency shall control all remote accesses through managed access control points. The agency may permit remote access for privileged functions only for compelling operational needs but shall document the rationale for such access in the security plan for the information system. [Original CJIS Reference - Policy Area 5: Access Control]",
      "requirement-status": "Medium",
      "regulation-name": "CJIS"
    },
    {
      "requirement-uid": "9918ec25-60e7-4a59-8fd4-a6ca01f87322",
      "requirement-id": "210007",
      "requirement-description": "The provision of access involves the following process stages: (a) identification and authentication: determination of who or what is requesting access and confirmation of the purported identity; (b) authorisation: assessment of whether access is allowed to an IT asset by the requestor based on the needs of the business and the level of IT security (trust) required. Identification, authentication and access authorisation processes are applicable to both users and IT assets. [Prudential Practice Guide: PPG 234, Access Control - Access based on business need - Requirement 39.]",
      "requirement-status": "Poor",
      "regulation-name": "PPG 234"
    },
    {
      "requirement-uid": "077cf39b-bcc8-4524-a4e3-cf5747e5d0c4",
      "requirement-id": "19. (3)",
      "requirement-description": "The responsible party must have due regard to generally accepted information security practices and procedures which may apply to it generally or be required in terms of specific industry or professional rules and regulations. (Original reference is Chapter 3 - Conditions for Lawful Processing of Personal Information, Condition 7 - Security Safeguards, Requirement 19 - Security measures on integrity and confidentiality of personal information.)",
      "requirement-status": "Good",
      "regulation-name": "Protection of Personal Information Act, 2013"
    },
    {
      "requirement-uid": "793bac66-310d-44c2-bb8b-5a922ac1408c",
      "requirement-id": "210008",
      "requirement-description": "A regulated institution would normally take appropriate measures to identify and authenticate users or IT assets. The required strength of authentication would normally be commensurate with risk. [Prudential Practice Guide: PPG 234, Access Control - Identification and authentication techniques - Requirement 40.]",
      "requirement-status": "Poor",
      "regulation-name": "PPG 234"
    },
    {
      "requirement-uid": "a35e43f4-f4f3-4fb0-a4ca-3166c5ed0c9a",
      "requirement-id": "210065",
      "requirement-description": "Common monitoring processes include: Checks to determine if IT security controls are operating as expected and are being complied with. [Prudential Practice Guide: PPG 234, Monitoring and incident management - Monitoring processes - Requirement 66 (c).]",
      "requirement-status": "Good",
      "regulation-name": "PPG 234"
    },
    {
      "requirement-uid": "1b736cde-91d1-471c-9fd3-fa43848d96b6",
      "requirement-id": "210020",
      "requirement-description": "A regulated institution would typically deploy the following controls to limit access to IT assets, based on a risk assessment: (i) multi-factor authentication for privileged access, remote access and other high-risk activities. [Prudential Practice Guide: PPG 234, Access Control - Access control techniques - Requirement 44 (i).]",
      "requirement-status": "Poor",
      "regulation-name": "PPG 234"
    },
    {
      "requirement-uid": "b0141b61-ad34-4447-ade0-d03a1da102cd",
      "requirement-id": "190116",
      "requirement-description": "8.3: Incorporate two-factor authentication for remote network access originating from outside the network by personnel (including users and administrators) and all third parties, (including vendor access for support or maintenance). [Original PCI DSS 3.0 Reference: 8.3]",
      "requirement-status": "Poor",
      "regulation-name": "PCI DSS 3.0"
    },
    {
      "requirement-uid": "c7f4bde2-d3df-471d-a212-8827cb30f070",
      "requirement-id": "02-VPN (1)",
      "requirement-description": "The IPSec VPN Software Blade must be securely configured in line with vendor recommendations.",
      "requirement-status": "Good",
      "regulation-name": "Statement of Controls (ISAE 3402)"
    },
    {
      "requirement-uid": "e9b483bd-40e9-4c89-adca-e5f02790f4cb",
      "requirement-id": "19. (2) (c)",
      "requirement-description": "The responsible party must take reasonable measures to regularly verify that the safeguards are effectively implemented. (Original reference is Chapter 3 - Conditions for Lawful Processing of Personal Information, Condition 7 - Security Safeguards, Requirement 19 - Security measures on integrity and confidentiality of personal information.)",
      "requirement-status": "Good",
      "regulation-name": "Protection of Personal Information Act, 2013"
    },
    {
      "requirement-uid": "01d2c888-a901-493f-a3ca-0909fa4fd5b9",
      "requirement-id": "11-GLO (1)",
      "requirement-description": "Remote Access must be encrypted and securely authenticated in line with vendor recommendations.",
      "requirement-status": "Good",
      "regulation-name": "Statement of Controls (ISAE 3402)"
    },
    {
      "requirement-uid": "7fef58b1-57e2-4a46-a9ff-ffc400e8074b",
      "requirement-id": "19. (1) (b)",
      "requirement-description": "A responsible party must secure the integrity and confidentiality of personal information in its possession or under its control by taking appropriate, reasonable technical and organisational measures to prevent unlawful access to or processing of personal information. (Original reference is Chapter 3 - Conditions for Lawful Processing of Personal Information, Condition 7 - Security Safeguards, Requirement 19 - Security measures on integrity and confidentiality of personal information.)",
      "requirement-status": "Good",
      "regulation-name": "Protection of Personal Information Act, 2013"
    },
    {
      "requirement-uid": "53ca9eb3-9a0e-4e3b-aa12-960dbd0af712",
      "requirement-id": "19. (2) (d)",
      "requirement-description": "The responsible party must take reasonable measures to ensure that the safeguards are continually updated in response to new risks or deficiencies in previously implemented safeguards. (Original reference is Chapter 3 - Conditions for Lawful Processing of Personal Information, Condition 7 - Security Safeguards, Requirement 19 - Security measures on integrity and confidentiality of personal information.)",
      "requirement-status": "Good",
      "regulation-name": "Protection of Personal Information Act, 2013"
    },
    {
      "requirement-uid": "8c56cd30-a8ba-4d1f-b83b-e711b674c9e0",
      "requirement-id": "19. (2) (b)",
      "requirement-description": "The responsible party must take reasonable measures to establish and maintain appropriate safeguards against the risks identified. (Original reference is Chapter 3 - Conditions for Lawful Processing of Personal Information, Condition 7 - Security Safeguards, Requirement 19 - Security measures on integrity and confidentiality of personal information.)",
      "requirement-status": "Good",
      "regulation-name": "Protection of Personal Information Act, 2013"
    },
    {
      "requirement-uid": "994516a8-2eaa-4001-9ac9-bf796dba5d80",
      "requirement-id": "32",
      "requirement-description": "Security of processing - Maintain procedures to restrict access to personal data (e.g. role-based access, segregation of duties)",
      "requirement-status": "Good",
      "regulation-name": "GDPR"
    },
    {
      "requirement-uid": "89ca40ff-ab40-4334-8a05-0aee1a4d64b2",
      "requirement-id": "500.02",
      "requirement-description": "Covered entities must maintain a cybersecurity program designed to protect the confidentiality, integrity and availability of the entitys information systems.�The program must be based on the entitys risk assessment and must be designed to (1) identify and assess internal and external cybersecurity risks that may threaten the security or integrity of nonpublic information stored on the entitys information systems; (2) use defensive infrastructure and policies and procedures to protect the entitys information systems from unauthorized access, use or other malicious acts; (3) detect cybersecurity events; (4) respond to identified or detected cybersecurity events to mitigate any negative effects; (5) recover from cybersecurity events and restore normal operations and services; and (6) fulfill applicable regulatory reporting obligations.",
      "requirement-status": "Good",
      "regulation-name": "New York State Cybersecurity Regulation"
    },
    {
      "requirement-uid": "50e20748-d46f-4b56-944b-fa70c440366a",
      "requirement-id": "190116",
      "requirement-description": "8.3.1: Secure all individual non-console administrative access and all remote access to the CDE using multi-factor authentication. [Original PCI DSS 3.2 Reference: 8.3.1]",
      "requirement-status": "Poor",
      "regulation-name": "PCI-DSS 3.2"
    },
    {
      "requirement-uid": "506bb84c-6b08-4551-9e7f-7628d0f419ce",
      "requirement-id": "190055",
      "requirement-description": "4.1: Use strong cryptography and security protocols to safeguard sensitive cardholder data during transmission over open, public networks, including the following: 1) Only trusted keys and certificates are accepted, 2) The protocol in use only supports secure versions or configurations, or 3) The encryption strength is appropriate for the encryption methodology in use. [Original PCI DSS 3.2 Reference: 4.1]",
      "requirement-status": "Good",
      "regulation-name": "PCI-DSS 3.2"
    },
    {
      "requirement-uid": "f1cae965-840b-49b1-a97b-9e41fdba3e63",
      "requirement-id": "190117",
      "requirement-description": "8.3.2: Incorporate multi-factor authentication for all remote network access (both user and administrator, and including third-party access for support or maintenance) originating from outside the entity's network. [Original PCI DSS 3.2 Reference: 8.3.2]",
      "requirement-status": "Poor",
      "regulation-name": "PCI-DSS 3.2"
    },
    {
      "requirement-uid": "707a65b8-9c9f-452e-bc0e-fc6279b7986c",
      "requirement-id": "CSC 12-12",
      "requirement-description": "Use multifactor authentication for all administrative access, including domain administrative access. Multi-factor authentication can include a variety of techniques, to include the use of smart cards with certificates, One Time Password (OTP) tokens, and biometrics. Taken from SANS Critical Control 12: Controlled Use of Administrative Privileges, Category: Configuration / Hygiene.",
      "requirement-status": "Poor",
      "regulation-name": "SANS Top 20"
    },
    {
      "requirement-uid": "b923d5da-d861-4669-8280-ee6c52f43cbf",
      "requirement-id": "AC.17.1",
      "requirement-description": "REMOTE ACCESS | AUTOMATED MONITORING / CONTROL The information system monitors and controls remote access methods.",
      "requirement-status": "Good",
      "regulation-name": "Canadian IT Security Risk Management: A Lifecycle Approach"
    },
    {
      "requirement-uid": "2cda6b0a-7b3d-40e6-8314-ebfb748e3d4a",
      "requirement-id": "AC.17",
      "requirement-description": "(A) The organization establishes and documents usage restrictions, configuration/connection requirements, and implementation guidance for each type of remote access allowed. (B) The organization authorizes remote access to the information system prior to allowing such connections. (AA) The organization ensures that all employees working off site safeguard information as per the minimum requirements in accordance with the TBS Operational Security Standard on Physical Security [Reference 6].",
      "requirement-status": "Good",
      "regulation-name": "Canadian IT Security Risk Management: A Lifecycle Approach"
    },
    {
      "requirement-uid": "b704eec1-77ff-46ab-ad83-7c4b1d58fa48",
      "requirement-id": "16",
      "requirement-description": "4.1: Use strong cryptography and security protocols (for example, SSL/TLS, IPSEC, SSH, etc.) to safeguard sensitive cardholder data during transmission over open, public networks, including the following: 1) Only trusted keys and certificates are accepted. 2) The protocol in use only supports secure versions or configurations. 3) The encryption strength is appropriate for the encryption methodology in use. [Original PCI DSS 3.0 Reference: 4.1]",
      "requirement-status": "Good",
      "regulation-name": "PCI DSS 3.2.1"
    },
    {
      "requirement-uid": "99acb5cb-e97f-4f75-9162-eb59be4602bb",
      "requirement-id": "28",
      "requirement-description": "8.3: Incorporate two-factor authentication for remote network access originating from outside the network by personnel (including users and administrators) and all third parties, (including vendor access for support or maintenance). [Original PCI DSS 3.0 Reference: 8.3]",
      "requirement-status": "Poor",
      "regulation-name": "PCI DSS 3.2.1"
    },
    {
      "requirement-uid": "3e9c4bf1-d1c9-4f6b-ad58-f45dc57e10fb",
      "requirement-id": "461",
      "requirement-description": "Payment Card Industry Data Security Standard (PCI-DSS)",
      "requirement-status": "Good",
      "regulation-name": "SAMA Cybersecurity framework"
    },
    {
      "requirement-uid": "2076a803-8a2c-444a-a942-cb5347a0de52",
      "requirement-id": "477",
      "requirement-description": "Password management system - Password management systems shall be interactive and shall  ensure quality passwords.",
      "requirement-status": "Medium",
      "regulation-name": "ISO 27001:2013"
    },
    {
      "requirement-uid": "1d88e614-7227-444a-a11e-2922fbe632af",
      "requirement-id": "469",
      "requirement-description": "Vulnerability Management - To ensure timely identification and effective mitigation of application and infrastructure vulnerabilities in order to reduce the likelihood and business impact for the Member Organization.",
      "requirement-status": "Good",
      "regulation-name": "SAMA Cybersecurity framework"
    },
    {
      "requirement-uid": "cebc489e-26d0-49cd-90a6-e6227dc0fe35",
      "requirement-id": "4718",
      "requirement-description": "Teleworking - A policy and supporting security measures shall be implemented to protect information accessed, processed or stored at teleworking sites.",
      "requirement-status": "Good",
      "regulation-name": "ISO 27001:2013"
    },
    {
      "requirement-uid": "a7216483-b05a-47a0-bee5-2fa01703dba8",
      "requirement-id": "463",
      "requirement-description": "To ensure that the Member Organization only provides authorized and sufficient access privileges to approved users.",
      "requirement-status": "Medium",
      "regulation-name": "SAMA Cybersecurity framework"
    },
    {
      "requirement-uid": "e472fd93-07bf-4cb2-9248-326da38da18d",
      "requirement-id": "4610",
      "requirement-description": "The effectiveness of the BYOD cyber security controls should be measured and periodically evaluated.",
      "requirement-status": "Good",
      "regulation-name": "SAMA Cybersecurity framework"
    },
    {
      "requirement-uid": "07e35f42-7e19-4139-9903-cde3a31312fb",
      "requirement-id": "471",
      "requirement-description": "Network controls - Networks shall be managed and controlled to protect information in systems and applications.",
      "requirement-status": "Good",
      "regulation-name": "ISO 27001:2013"
    },
    {
      "requirement-uid": "d41038c4-5f48-415f-ae52-e8c668bde214",
      "requirement-id": "464",
      "requirement-description": "To support that all cyber security controls within the infrastructure are formally documented and the  compliance is monitored and its effectiveness is evaluated periodically within the Member Organization.",
      "requirement-status": "Good",
      "regulation-name": "SAMA Cybersecurity framework"
    },
    {
      "requirement-uid": "4c460222-5875-487c-8f8c-d8e67c7f2b3b",
      "requirement-id": "D2f",
      "requirement-description": "Your organisation must proactively manage your computers and network devices. You must regularly: ensure appropriate device locking controls (see device unlocking, below) for users that are physically present (such as logging on to a laptop or unlocking a mobile phone), a credential such as a biometric, password or PIN must be in place before a user can gain access to the services.",
      "requirement-status": "Medium",
      "regulation-name": "Cyber Essentials v3.1"
    },
    {
      "requirement-uid": "1190e74e-31cf-490e-9b11-416bbce84491",
      "requirement-id": "12.2",
      "requirement-description": "The organization establishes and maintains a security system to protect the corporate communication network.",
      "requirement-status": "Good",
      "regulation-name": "Israeli Cyber Defence Methodology 2.0"
    },
    {
      "requirement-uid": "147ef46c-55a8-4aa8-90a1-6a961fd133ea",
      "requirement-id": "D2e",
      "requirement-description": "Your organisation must proactively manage your computers and network devices. You must regularly: ensure users are authenticated before allowing them access to organisational data or services",
      "requirement-status": "Poor",
      "regulation-name": "Cyber Essentials v3.1"
    },
    {
      "requirement-uid": "339a30c0-d522-4c25-a003-7277c6880c30",
      "requirement-id": "2.1.4",
      "requirement-description": "The requirements for teleworking are determined and fulfilled. The following aspects are considered:   - Secure handling of and access to information (in both electronic and paper form) while considering the protection needs and the contractual requirements applying to private (e.g. home office) and public surroundings (e.g. during travels),   - Behavior in private surroundings,   - Behavior in public surroundings,   - Measures for protection from theft (e.g. in public surroundings),  The organization network is accessed via a secured connection (e.g. VPN) and strong authentication.  Protective measures against overhearing and viewing are implemented.",
      "requirement-status": "Good",
      "regulation-name": "TISAX 5.1"
    },
    {
      "requirement-uid": "6cdbcdc9-9390-482f-8269-488ddf469405",
      "requirement-id": "C038_7",
      "requirement-description": "Level 3: SC.3.185 Implement cryptographic mechanisms to prevent unauthorized disclosure of CUI during transmission unless otherwise protected by alternative physical safeguards. , NIST SP 800-171 Rev 1 3.13.8 , NIST CSF v1.1 PR.AC-2 , CERT RMM v1.2 KIM:SG4.SP1 , NIST SP 800-53 Rev 4 SC-8(1).",
      "requirement-status": "Good",
      "regulation-name": "Cybersecurity Maturity Model Certification"
    },
    {
      "requirement-uid": "e7e98cf6-20d7-4279-bd3c-4a860c742411",
      "requirement-id": "NET1",
      "requirement-description": "Deny corporate computers direct internet connectivity. Use a gateway firewall to require use of a split DNS server, an email server and an authenticated web proxy server for outbound web connections.",
      "requirement-status": "Good",
      "regulation-name": "Essential Eight & Strategies to Mitigate Cyber Security Incidents"
    },
    {
      "requirement-uid": "3dc6e5b6-63f0-409e-a16f-9b0376bb1d10",
      "requirement-id": "7.6",
      "requirement-description": "Perform automated vulnerability scans of externally-exposed enterprise assets using a SCAP-compliant vulnerability scanning tool. Perform scans on a monthly, or more frequent, basis.",
      "requirement-status": "Good",
      "regulation-name": "Center for Internet Security Benchmarks"
    },
    {
      "requirement-uid": "f3735335-6853-425c-a4b8-e573f38d0b99",
      "requirement-id": "ART21.d",
      "requirement-description": "Remote Access",
      "requirement-status": "Good",
      "regulation-name": "Network and Information Systems Directive 2"
    },
    {
      "requirement-uid": "cd2d5fce-0488-4e4c-998c-d1339b41386c",
      "requirement-id": "6.4",
      "requirement-description": "Require MFA for remote network access.",
      "requirement-status": "Medium",
      "regulation-name": "Center for Internet Security Benchmarks"
    },
    {
      "requirement-uid": "23dcca86-b206-48e5-9a26-66d0153e38c8",
      "requirement-id": "AUTH1",
      "requirement-description": "Multi-factor authentication especially for Most Likely Targets, VPNs, RDP, SSH and other remote access capabilities, and for all users when they perform a privileged action (including system administration) or access an important (sensitive or high-availability) data repository.  Multi-factor authentication is used to authenticate users to their organisations online services that process, store or communicate their organisations sensitive data.",
      "requirement-status": "Good",
      "regulation-name": "Essential Eight & Strategies to Mitigate Cyber Security Incidents"
    },
    {
      "requirement-uid": "e14c58b6-91f3-456e-aa3d-8335538358bb",
      "requirement-id": "12.7",
      "requirement-description": "Require users to authenticate to enterprise-managed VPN and authentication services prior to accessing enterprise resources on end-user devices.",
      "requirement-status": "Poor",
      "regulation-name": "Center for Internet Security Benchmarks"
    },
    {
      "requirement-uid": "610bb2f4-a2c4-4516-9c67-866a6ad99e4e",
      "requirement-id": "3.10",
      "requirement-description": "Encrypt sensitive data in transit. Example implementations can include: Transport Layer Security (TLS) and Open Secure Shell (OpenSSH).",
      "requirement-status": "Medium",
      "regulation-name": "Center for Internet Security Benchmarks"
    },
    {
      "requirement-uid": "60653025-6b1f-43bd-a087-82bebf86d577",
      "requirement-id": "4.4.3.2",
      "requirement-description": "The managing organization shall periodically evaluate  the overall CSMS to ensure the security objectives are  being met",
      "requirement-status": "Good",
      "regulation-name": "IEC 62443-2-1 2010"
    },
    {
      "requirement-uid": "c53bc566-7577-4b3d-ad88-bec148ce4a67",
      "requirement-id": "4.3.3.6.2",
      "requirement-description": "All users shall be authenticated before using the requested  application, unless there are compensating combinations of  entrance control technologies and administrative practices",
      "requirement-status": "Poor",
      "regulation-name": "IEC 62443-2-1 2010"
    },
    {
      "requirement-uid": "5b703aac-6f18-465c-b8bc-720934fb7af4",
      "requirement-id": "4.3.3.4.3",
      "requirement-description": "Barrier devices shall block all non-essential communications in and  out of the security zone containing critical control equipment",
      "requirement-status": "Good",
      "regulation-name": "IEC 62443-2-1 2010"
    },
    {
      "requirement-uid": "b9812725-b775-483e-9eae-9be5bbd0c60a",
      "requirement-id": "1.5.1",
      "requirement-description": "Security controls are implemented on any computing devices, including company- and employee-owned devices, that connect to both untrusted networks (including the Internet) and the CDE as follows: Specific configuration settings are defined to prevent threats being introduced into the entitys network. Security controls are actively running. Security controls are not alterable by users of the computing devices unless specifically documented and authorized by management on a case-by-case basis for a limited period.",
      "requirement-status": "Good",
      "regulation-name": "PCI DSS 4.0"
    },
    {
      "requirement-uid": "05b250a3-00e4-4f47-90c8-5f8ce62f4092",
      "requirement-id": "1.4.5",
      "requirement-description": "The disclosure of internal IP addresses and routing information is limited to only authorized parties.",
      "requirement-status": "Good",
      "regulation-name": "PCI DSS 4.0"
    },
    {
      "requirement-uid": "5433b450-3d90-475d-ae0e-96ee5132393e",
      "requirement-id": "8.4.3",
      "requirement-description": "MFA is implemented for all remote network access originating from outside the entitys network that could access or impact the CDE as follows: All remote access by all personnel, both users and administrators, originating from outside the entitys network. All remote access by third parties and vendors.",
      "requirement-status": "Poor",
      "regulation-name": "PCI DSS 4.0"
    },
    {
      "requirement-uid": "cee6c1a3-12f1-4161-b681-129434895dd3",
      "requirement-id": "4.2.1",
      "requirement-description": "Strong cryptography and security protocols are implemented as follows to safeguard PAN during transmission over open, public networks: Only trusted keys and certificates are accepted. Certificates used to safeguard PAN during transmission over open, public networks are confirmed as valid and are not expired or revoked. This bullet is a best practice until its effective date; refer to applicability notes below for details. The protocol in use supports only secure versions or configurations and does not support fallback to, or use of insecure versions, algorithms, key sizes, or implementations. The encryption strength is appropriate for the encryption methodology in use.",
      "requirement-status": "Good",
      "regulation-name": "PCI DSS 4.0"
    },
    {
      "requirement-uid": "5b24c9ee-908a-4769-8f83-fd46195b16f3",
      "requirement-id": "8.5",
      "requirement-description": "Secure Authentication - Secure authentication technologies and procedures should be implemented based on information access restrictions and the topic-specific policy on access control.",
      "requirement-status": "Good",
      "regulation-name": "ISO 27001:2022"
    },
    {
      "requirement-uid": "ef99ce8c-d713-43c8-be12-0757531fdf6d",
      "requirement-id": "5.1.2",
      "requirement-description": "With respect to the CIIOs obligations under clause 5.1.1, the CIIO shall put in place authorisation and authentication controls for any access to the CII and between parts of the CII commensurate with the cybersecurity risk profile of the CII.",
      "requirement-status": "Medium",
      "regulation-name": "CSA CCoP 2.0"
    },
    {
      "requirement-uid": "6333aed8-7637-4c70-bae8-cf5859e4cff3",
      "requirement-id": "9.4",
      "requirement-description": "c. implement policies that limit the physical or logical access to information assets and ICT assets to what is required for legitimate and approved functions and activities only, and establish to that end a set of policies, procedures and controls that address access rights and ensure a sound administration thereof d. implement policies and protocols for strong authentication mechanisms, based on relevant standards and dedicated control systems, and protection measures of cryptographic keys whereby data is encrypted based on results of approved data classification and ICT risk assessment processes;",
      "requirement-status": "Good",
      "regulation-name": "DORA:2023"
    },
    {
      "requirement-uid": "27d3df89-38f6-4f1c-9fec-4ba742bc7f5a",
      "requirement-id": "9.3",
      "requirement-description": "a. ensure the security of the means of transfer of data b. minimise the risk of corruption or loss of data, unauthorised access and technical flaws that may hinder business activity c. prevent the lack of availability, the impairment of the authenticity and integrity, the breaches of confidentiality and the loss of data",
      "requirement-status": "Poor",
      "regulation-name": "DORA:2023"
    },
    {
      "requirement-uid": "9396f4d5-f370-4d94-9bd3-c5c42ce1db64",
      "requirement-id": "5.7",
      "requirement-description": "The CIIO shall ensure that: (a) Remote connections to the CII are disabled except where necessary for operating the CII; (b) Multi-factor authentication is required for the establishing a remote connection to the CII; (c) Remote connections to the CII have strong encryption and are made only through secured intermediary mechanisms; (d) Measures are put in place to ensure transmission security and message integrity over the remote connection; (e) Files to be uploaded to the CII are scanned for malware before being uploaded; and (f) Data flows over remote connections to the CII are limited to only the minimum necessary for performing the function required of the connection.",
      "requirement-status": "Good",
      "regulation-name": "CSA CCoP 2.0"
    },
    {
      "requirement-uid": "e51ac170-bb29-4815-a7ea-ed2760096e68",
      "requirement-id": "5.9.1-2",
      "requirement-description": "In respect of the following types of CII assets as they may be found in the CII, the CIIO shall establish and implement a security configuration baseline for each asset that is commensurate with the cybersecurity risk profile of the CII: (a) Operating systems; (b) Appliances; (c) Consoles and workstations, including Human Machine Interfaces (HMI) and OT engineering workstations; (d) Network devices; (e) Servers, including alarm servers, OT historians and management servers; (f) Software applications; and (g) Any other CII asset or type of asset identified by the Commissioner. The security configuration baselines shall minimally address the following security practices: (a) Account management - disable or remove default accounts, guest accounts, inactive accounts and unused accounts; (b) Password and passphrase management - Default passwords shall be changed; passwords and passphrases shall be stored using in their hash forms; (c) Application control - Disable services and remove applications that are not necessary for the operation of the CII; (d) Port(s) and service(s) management - Enable only ports and services that are necessary for the operation of the CII; (e) Physical connection - Enable only external physical connections that are necessary for the operation of the CII; (f) Malware protection - Install and update to the latest version of anti-malware software with the latest anti-malware signatures; and (g) Software upgrade and update - Timely upgrade and update of software and security patches.",
      "requirement-status": "Good",
      "regulation-name": "CSA CCoP 2.0"
    },
    {
      "requirement-uid": "e2b19c81-10dc-41e2-8a81-aaa789f81674",
      "requirement-id": "8.21",
      "requirement-description": "Security mechanisms, service levels and service requirements of network services should be identified, implemented and monitored.",
      "requirement-status": "Medium",
      "regulation-name": "ISO/IEC 27002:2022"
    },
    {
      "requirement-uid": "2d42e4e9-9634-43dd-9cba-5b4d4d070111",
      "requirement-id": "8.5",
      "requirement-description": "Secure authentication technologies and procedures should be implemented based on information access restrictions and the topic-specific policy on access control.",
      "requirement-status": "Good",
      "regulation-name": "ISO/IEC 27002:2022"
    },
    {
      "requirement-uid": "1c5fd057-6632-432b-a410-a19c669dbb42",
      "requirement-id": "F.7.17 SC8",
      "requirement-description": "Transmission Confidentiality and Integrity Protect the confidentiality; integrity of transmitted information",
      "requirement-status": "Medium",
      "regulation-name": "NIST800-82r3"
    },
    {
      "requirement-uid": "ecd773dc-c854-4631-a46b-faa6b5ce31b5",
      "requirement-id": "F.7.17 SC7",
      "requirement-description": "Boundary Protection a. Monitor and control communications at the external managed interfaces to the system and at key internal managed interfaces within the system; b. Implement subnetworks for publicly accessible system components that are physically; logically separated from internal organizational networks; and c. Connect to external networks or systems only through managed interfaces consisting of boundary protection devices arranged in accordance with an organizational security and privacy architecture.",
      "requirement-status": "Good",
      "regulation-name": "NIST800-82r3"
    },
    {
      "requirement-uid": "d1aeb4de-55f3-4807-9b09-7a03f1847720",
      "requirement-id": "F.7.7 IA3",
      "requirement-description": "Device Identification and Authentication Uniquely identify and authenticate [Assignment: organization-defined devices and/or types of devices] before establishing alocal; remote; network connection",
      "requirement-status": "Good",
      "regulation-name": "NIST800-82r3"
    },
    {
      "requirement-uid": "e8c0b14b-f633-4912-983e-08f7ba9dc1b6",
      "requirement-id": "F.7.1 AC17",
      "requirement-description": "Remote Access Establish and document usage restrictions, configuration/connection requirements, and implementation guidance for each type of remote access allowed",
      "requirement-status": "Good",
      "regulation-name": "NIST800-82r3"
    }
  ]
}
```
