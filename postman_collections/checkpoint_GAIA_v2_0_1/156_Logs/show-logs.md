# show-logs

**Collection:** Web API (version 2.0.1) > 156 Logs
**Method:** `POST`
**URL:** `{{server}}/v2.0.1/show-logs`

## Description

Querying for logs with a simple filter. To be able to use the show logs with paging command, you must include the session id in the command.

## Request Headers

| Header | Value |
|--------|-------|
| Content-Type |  application/json |
| X-chkp-sid |  {{session}} |

## Request Body

**Mode:** `raw`

```json
{
  "new-query": {
    "time-frame": "today",
    "max-logs-per-request": "2",
    "filter": "blade:Threat Emulation"
  }
}
```

## Example Responses

### Example 1: show-logs
**Status:** `200 OK`

**Body:**
```javascript
{
  "logs": [
    {
      "analyzed_on": "Check Point Threat Cloud",
      "i_f_dir": "inbound",
      "proto_attr": [
        {
          "isCHKPObject": "false",
          "resolved": "TCP (6)"
        }
      ],
      "type": "Log",
      "orig_log_server_attr": [
        {
          "isCHKPObject": "true",
          "uuid": "ac0f97df-be60-744c-b2c0-4b39d2f35d1b",
          "resolved": "harry-api-for-logs-t261-take-13"
        }
      ],
      "index_time": "2020-03-29T14:01:13Z",
      "policy_date": "2019-06-30T10:02:43Z",
      "file_type": "pdf",
      "file_md5": "c0d5b1cc0c77fcf32ff02aac98fac536",
      "dst_attr": [
        {
          "isCHKPObject": "false",
          "resolved": "labs-proxy-old.ad.checkpoint.com"
        }
      ],
      "action": "Detect",
      "id": "ac17545d-440a-0000-5e80-a70500000000",
      "i_f_name": "eth0",
      "lastUpdateSeqNum": "3",
      "sequencenum": "3",
      "resource": "http://192.168.13.178/sari/mainte/Evgeny_CV_m.pdf",
      "rounded_sent_bytes": "0",
      "policy_time": "2019-06-30T10:02:44Z",
      "TP_match_table": [
        {
          "smartdefense_profile": "kobi",
          "layer_name": "Standard Threat Prevention",
          "layer_uuid": "B267F23C-FF59-4062-923F-605C371D15D3",
          "malware_rule_id": "38AA1A71-9BB4-4A14-BC35-B138262A707D"
        }
      ],
      "marker": "@A@@B@1585515600@C@34",
      "log_uid": "DCB3FC1C-2517-314A-9B1E-E992202D7AAE",
      "proto": "6",
      "verdict": "Malicious",
      "protection_name": "Exploited pdf document",
      "te_verdict_determined_by": "Win7,Office 2013,Adobe 11: cloud emulation. WinXP,Office 2003/7,Adobe 9: cloud emulation. ",
      "packet_capture_unique_id": [
        "{DCB3FC1C-2517-314A-9B1E-E992202D7AAE}00000000-0000-0000-0000-000000000000",
        "{DCB3FC1C-2517-314A-9B1E-E992202D7AAE}e50e99f3-5963-4573-af9e-e3f4750b55e2"
      ],
      "policy_mgmt": "halo1-main-take-101",
      "lastUpdateTime": "1585489669000",
      "dst": "194.29.36.43",
      "confidence_level": "High",
      "description": "Malicious embedded file detected: File Type: js, File SHA-1: bc00b5378dbe753cff283be71c049551ef892161.",
      "source_os": "Windows",
      "file_sha256": "e68f38195b3c816309882388c23118327ec97f9ad775bf59b9a8a3089dd68fd8",
      "__interface": "eth0",
      "resource_table": [
        {
          "resource": "http://192.168.13.178/sari/mainte/Evgeny_CV_m.pdf"
        }
      ],
      "scope": "10.0.0.90",
      "detected_on": [
        "WinXP,Office 2003/7,Adobe 9",
        "Win7,Office 2013,Adobe 11"
      ],
      "malware_rule_id": "38AA1A71-9BB4-4A14-BC35-B138262A707D",
      "rounded_received_bytes": "0",
      "policy": "Standard",
      "proxy_src_ip": "10.0.0.90",
      "dst_country": "Israel",
      "severity": "Critical",
      "s_port": "49511",
      "log_id": "4000",
      "product_family": "Threat",
      "product": "Threat Emulation",
      "file_sha1": "2154845e38fc348ae1be419684f9572a680fabfd",
      "src": "10.0.0.90",
      "smartdefense_profile": "kobi",
      "file_name": "Evgeny_CV_m.pdf",
      "session_id": "0xdcb3fc1c,0x2517314a,0x9b1ee992,0x202d7aae",
      "policy_name": "Standard",
      "protection_type": "HTTP Emulation",
      "file_size": "213354",
      "db_tag": "{8C228E1C-4D2C-624E-8A2A-C12DE7EF4641}",
      "orig_log_server": "172.23.84.93",
      "fservice": "HTTPS_proxy",
      "orig": "dummyGW",
      "service": "8080",
      "rounded_bytes": "0",
      "orig_log_server_ip": "172.23.84.93",
      "stored": "true",
      "malware_action": [
        "Unexpected Process Termination",
        "Unexpected Process Creation"
      ],
      "calc_desc": "10.0.0.90 downloaded a malicious file from http://192.168.13.178/sari/mainte/evgeny_cv_m.pdf that was detected",
      "time": "2020-03-29T13:47:49Z",
      "packet_capture": "Packet Capture"
    },
    {
      "analyzed_on": "Check Point Threat Cloud",
      "i_f_dir": "inbound",
      "proto_attr": [
        {
          "isCHKPObject": "false",
          "resolved": "TCP (6)"
        }
      ],
      "detection_time": "2016-01-31T04:06:08Z",
      "type": "Correlated",
      "time_interval": "0",
      "orig_log_server_attr": [
        {
          "isCHKPObject": "true",
          "uuid": "ac0f97df-be60-744c-b2c0-4b39d2f35d1b",
          "resolved": "harry-api-for-logs-t261-take-13"
        }
      ],
      "cu_detected_by": "192.168.32.125",
      "index_time": "2020-03-29T13:39:08Z",
      "is_last": "1",
      "file_type": "xls",
      "file_md5": "59e131ab59885898620f9b5f2e5024a7",
      "dst_attr": [
        {
          "isCHKPObject": "false",
          "resolved": "labs-proxy-old.ad.checkpoint.com"
        }
      ],
      "action": "Detect",
      "id": "ac17545d-2f60-0000-5e80-a4ef00000049",
      "i_f_name": "<null>",
      "lastUpdateSeqNum": "147",
      "sequencenum": "147",
      "rounded_sent_bytes": "0",
      "cu_log_count": "2",
      "cu_rule_category": "Legacy;Threat Prevention",
      "last_update_time": "2016-01-31T04:06:08Z",
      "marker": "@A@@B@1585489134@C@181",
      "proto": "6",
      "verdict": "Malicious",
      "protection_name": "Exploited xls document",
      "event_name": "Threat Emulation",
      "packet_capture_unique_id": [
        "{0000006F-0061-004D-A2F6-68014A191CC6}00000000-0000-0000-0000-000000000000",
        "{0000006F-0061-004D-A2F6-68014A191CC6}e50e99f3-5963-4573-af9e-e3f4750b55e2"
      ],
      "lastUpdateTime": "1585489135000",
      "max_num_count_detected": "2",
      "dst": "194.29.36.43",
      "confidence_level": "High",
      "__interface": "<null>",
      "num_of_updates": "2",
      "event_start_time": "2016-01-31T04:06:07Z",
      "is_correlated": "true",
      "detected_on": [
        "WinXP,Office 2003/7,Adobe 9",
        "Win7,Office 2013,Adobe 11"
      ],
      "malware_rule_id": "427196B4-B437-44CB-9E82-AFCE9E55681C",
      "rounded_received_bytes": "0",
      "dst_country": "Israel",
      "severity": "Critical",
      "log_id": "2000",
      "product_family": "Threat",
      "file_sha1": "37ae372dd5a3cca351058cf1833f75c9a451c565",
      "product": "Threat Emulation",
      "src": "10.13.23.44",
      "file_name": "HP_600GB_SAS_15K_c.xls",
      "protection_type": "HTTP Emulation",
      "event_end_time": "2016-01-31T04:06:08Z",
      "orig_log_server": "172.23.84.93",
      "fservice": "http",
      "orig": "192.168.13.23",
      "service": "80",
      "rounded_bytes": "0",
      "orig_log_server_ip": "172.23.84.93",
      "stored": "true",
      "malware_action": [
        "Malware signature matched ( Virus.MSExcel.Sic.T.tb )",
        "Malware activity observed ( Virus.MSExcel.Sic.f )"
      ],
      "calc_desc": "10.13.23.44 downloaded a malicious file from  that was detected",
      "cu_rule_id": "BF24D5CC-931C-4583-A3C7-101A8ACD0532",
      "logid": "134217729",
      "time": "2020-03-29T13:38:55Z",
      "packet_capture": "Packet Capture"
    }
  ],
  "logs-count": "2",
  "query-id": "aa_be383957-9167-4ca3-b101-a25bc0fbec1c"
}
```
