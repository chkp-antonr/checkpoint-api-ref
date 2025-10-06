---
title: Introduction to the Check Point Management API
source_html: C:\_Labs\Dev\checkpoint-api-ref-py\out\html\introduction.html
generatedAt: '2025-10-05T18:45:55.690997+00:00'
---

# Introduction to the Check Point Management API
### Overview
R80 and above adds a new way to read information and to send commands to the Check Point management server.
Just like it is possible to create objects, work on the security policy using the SmartConsole GUI, it is now possible to do the same using command line tools and through web-services.
### Target audience
The management API was created with the following target audiences in mind:
* System administrators who wish to improve their productivity by scripting some of their daily tasks.
* Customers who wish to integrate the Check Point solution with other solutions that they have (virtualization servers, ticketing systems, change management systems, etc.).
* Check Point partners and integrators that look for an easy to use API that can help them create complementary products around the Check Point solution.
### Installation
The management APIs are installed as part of any R80 and above management server.
Follow the Check Point Jumbo Hotfix releases to keep track of the latest improvements to the Management APIs.
### Security Management Server and Multi-Domain Server
There are different domains for the Multi-Domain Server and the Security Management Server, and each domain has its own API calls:
* Multi-Domain Server - The default login is to the System Data domain. This allows you to manage administrators, domains and other system objects.
* To log in to a specific domain by name or IP address, use the domain parameter.
* To make Global Policy Updates, log in to the Global Domain.
* Security Management Server - The default login is to the SMC User domain. This allows you to manage objects and policies.
* To manage administrators and permission profiles, log in to the System Data domain.
### Using the Management APIs
There are four ways to communicate use the management APIs:
1. Typing API commands from a dialog inside the SmartConsole GUI application.
2. Typing API commands using the "mgmt\_cli" executable (available in both Windows, Linux/Gaia flavors).
3. Typing API commands using Gaia's secure shell (clish).
4. Sending API commands over an https connection using web-services
## Typing API commands from the SmartConsole GUI
Open the SmartConsole GUI and click the ![](images/api_icon.png) icon on the bottom left corner.
In the dialog that opens, you can now type API commands.
![](images/smartconsole.png)
Try the following commands:
* ```
add host name myHost ip-address 192.0.2.100
```
This will create a new host object with the name myHost and the IP address 192.0.2.100
* ```
add network name myNetwork subnet 192.0.2.0 subnet-mask 255.255.255.0
```
This will create a new network object with the name myNetwork for the network 192.0.2.0 and the subnet-mask
255.255.255.0.
If you prefer the CIDR notation, this command is equivalent:
```
add network name myNetwork subnet 192.0.2.0 mask-length 24
```
Notice that after typing these commands, the objects myHost and myNetwork appear on the objects panel on the
right side of the GUI.
A few more examples:
* ```
add group name myGroup members myHost
```
This will create a new group object and will include myHost a member of this group.
* ```
add host name "my second host" ip-address 192.168.0.101 groups myGroup
```
This command will create another host object and will make this new host a member of the myGroup group
object. Notice that the name of the host is surrounded with quotation marks this allows the 'name' argument
to have spaces in it.
For a complete list of all the available commands and their arguments check the API reference part in this document.
## Using the "mgmt\_cli" tool
The mgmt\_cli tool is installed as part of Gaia on all R80 and above gateways and can be used in scripts running in expert mode.
The mgmt\_cli.exe tool is installed as part of the R80 and above SmartConsole installation (e.g, typically under C:\Program Files (x86)\CheckPoint\SmartConsole\R81.20\PROGRAM\) and can be copied to run on any Windows machine.
For a complete list of the mgmt\_cli options, run "mgmt\_cli" and hit Enter.
Examples:
* ```
# mgmt_cli add host name host1 ip-address 192.0.2.100
```
The CLI will now prompt for username and then for password.
* ```
# mgmt_cli add host name host2 ip-address 192.0.2.101 -u myname
```
The CLI will now prompt for a password.
* ```
# mgmt_cli add host name host3 ip-address 192.0.2.102 -u myname -p secret
```
Both username and password are given in the command.
* ```
# mgmt_cli add host name host4 ip-address 192.0.2.103 -s id.txt
```
Session identifier is read from a previous login command response, stored in id.txt file.
* ```
# mgmt_cli add host name host5 ip-address 192.0.2.104 --session-id <session-id>
```
Session identifier is provided explicitly from a previous login command response ('sid' field).
* For additional possibilities to provide login credentials, refer to the "Login Command" section.
The mgmt\_cli tool uses the same syntax that is used inside the SmartConsole GUI but there is one important difference:
* When typing commands inside the GUI they just work - There is no need to provide a username, password or the ip-address of the management server because this information was already provided in the GUI’s login dialog and the commands are executed in that context. When using the mgmt\_cli tool, in order for a command to run, it is mandatory to provide login credentials or use a session-id token that was obtained previously using the ‘login’ command.
Calling mgmt\_cli with '-s' or '--session-id' flag will execute 'add host' command leaving it to user to publish (or discard) the changes.
Although calling mgmt\_cli with credentials (provided explicitly or entered by prompt) will result in performing four different operations:
* Log into the management server using the supplied credentials
* Execute the 'add host' command
* Publish
* Logout
### The login command
A login command creates a "session". All changes that happen during this session can be accepted (published) or dropped (discarded) according to your decision.
Login command examples:
**Example 1**
Login to the local management server using username and password
```
mgmt_cli login user me password secret
```
**Example 2**
Login to the local management server in short notation
```
mgmt_cli login -u me -p secret
```
**Example 3**
Login without username or password. CLI will prompt the user to provide them
```
mgmt_cli login
```
**Example 4**
Login into a remote management server located at 192.0.2.2
```
mgmt_cli login user me password secret -m 192.0.2.2
```
**Example 5**
Login into a management domain called “my domain” on a remote multi-domain server whose MDS IP-address is 192.0.2.2
```
mgmt_cli login user me password secret domain "my domain" -m 192.0.2.2
```
**Example 6**
Login into a management domain in short notation
```
mgmt_cli login -u me -p secret -d "my domain" -m 192.0.2.2
```
**Example 7**
If administrator logged into the management server and wants to receive SuperUser permissions,
"login-as-root" feature might be used. In this case providing additional login credentials is not required.
```
mgmt_cli login --root true
```
**Example 8**
Logging in as root in short notation
```
mgmt_cli login -r true
```
**Example 9**
Logging into the management server with a client certificate issued from the SmartConsole
```
mgmt_cli login --client-cert path-to-certificate-file.p12 password secret
```
**Example 10**
Logging with a client certificate in short notation
```
mgmt_cli login -c path-to-certificate.p12 -p secret
```
**Example 11**
Logging with a client certificate without password. CLI will prompt the user to provide it
```
mgmt_cli login -c path-to-certificate.p12
```
**Example 12**
Part of command parameters can be provided as environment variables.
| --- | --- | --- |
| Parameter name | Short name | Environment variable |
| User name | -u | MGMT\_CLI\_USER |
| Password | -p | MGMT\_CLI\_PASSWORD |
| Domain | -d | MGMT\_CLI\_DOMAIN |
| Client certificate path | -c | MGMT\_CLI\_CLIENT\_CERTIFICATE |
| Management server address | -m | MGMT\_CLI\_MANAGEMENT |
Login is called when username and password are declared as environment variables
```
export MGMT_CLI_USER=me
export MGMT_CLI_PASSWORD=secret
mgmt_cli login
```
A typical response from a successful login command looks like this:
```
sid: "R9kLPZ7vNTk9iBY8xHmGWpHJ2Kn25PqqUsvfIs5mBqw"
url: "https://192.0.2.2:443/web_api"
uid: "f0cb44d3-2d64-41cb-8026-219af70cb5bb"
session-timeout: 600
login-message:
header: "Warning"
message: "This system is for authorized use only"
```
* "sid" stands for "Session ID". Using the Session-ID token, subsequent CLI commands can communicate with the management server without going through the login process again.
* The "url" field points to the management server.
* The "session-timeout" field lists the number of idle seconds the management server will allow before disconnecting.
**Tip:**
* When creating a script that consists of a login command and other commands that share the login’s session-ID, you don’t need to figure out how to extract the session-ID value from the login command and pass it to the other commands.
You can redirect the output of the login command to a file and later have the rest of the mgmt\_cli commands use this file as an argument.
A simple bash script that logs into the management server and creates two host objects:
```
#!/bin/sh
mgmt_cli login user me password secret > id.txt
mgmt_cli add host name host1 ip-address 192.0.2.1 -s id.txt
mgmt_cli add host name h2 ip-address 192.0.2.2 -s id.txt
mgmt_cli publish -s id.txt
mgmt_cli logout -s id.txt
```
In the above example, the output from the login command is redirected to a file called "id.txt". By using the "-s" parameter, the rest of the commands read "id.txt" and automatically extract the session-id from this file.
Additional possibility to provide a session-ID to the command is by using the "--session-id" flag or MGMT\_CLI\_SESSION\_ID
environment variable.
**Tip:**
* In some cases, your script would like to parse the output of a mgmt\_cli command. Instead of using tools such as ‘grep’, ‘sed’, ‘cut’ and ‘awk’, a more elegant solution would be to ask the mgmt\_cli to produce the output using json format (--format json).
Once the output is in json format, you can use a tool called “jq” to do the parsing work for you.
The “jq” tool is installed on every Gaia machine at $CPDIR/jq/jq.
To learn more about jq, visit http://stedolan.github.io/jq/
Example:
```
#!/bin/sh
mgmt_cli login user me password secret > id.txt
mgmt_cli show hosts -s id.txt --format json > hosts.json
mgmt_cli logout -s id.txt
cat hosts.json | $CPDIR/jq/jq ".objects[] | .name"
```
The output of this script would be a list of all the host names.
## Using the Gaia CLI (clish)
To run management API commands in Gaia's shell, you need to log in as a management user first.
In Gaia's shell, type
```
mgmt login
```
or
```
mgmt login user myname
```
After that you remain in the familiar Gaia shell, but now you can use the management APIs.
Example:
```
> mgmt login user <admin name>
Enter password: ******
> show interfaces
eth0
eth0.3
lo
> mgmt add host name myHost12 ip-address 3.3.3.3
> mgmt publish
message "OK"
number-of-published-changes     1
>
```
* The syntax is identical to the commands that you run in the SmartConsole GUI.
* All management commands start with the word "mgmt".
## Using Web Services
Building applications that communicate with the Check Point management server has never been easier.
All that is needed is to send an HTTPS Post request to the management server.
### Web request structure
**HTTP Post to:**
```
https://<management server>:<port>/web_api/<command>
```
The default port number is 443
**HTTP Headers**
```
content-Type: application/json
```
```
x-chkp-sid: <session ID token as returned by the login command>
```
The x-chkp-sid header is mandatory in all API calls except the login API.
**Request payload**
```
Text in JSON format containing the different parameters
```
### Responset structure
Returned value on success:
* HTTP status 200
* A JSON string. The content varies depending on which API is called.
Returned value on failure:
* HTTP status 500
* A JSON structure with the error details.
### Login example:
**Request:**
```
HTTP Post to https://192.0.2.10/web_api/login
```
```
content-Type: application/json
```
```
{
"user":"me",
"password":"secret"
}
```
**Response:**
```
Status: 200 OK
```
```
{
"sid": "8478V00sYHvH_nBvIhDI203eu3clauAuB1iCEWOw_YY",
"url": "https://192.0.2.10:443/web_api",
"session-timeout": 600,
"last-login-was-at": {
"posix": 1430906758008,
"iso-8601": "2015-05-06T13:05+0300"
},
"last-login-from": "127.0.0.1",
"web-api-version": "1.0"
}
```
### Create host example:
**Request:**
```
HTTP Post to https://192.0.2.10/web_api/add-host
```
```
content-Type: application/json
X-chkp-sid:8478V00sYHvH_nBvIhDI203eu3clauAuB1iCEWOw_YY
```
```
{
"name":"MyHost",
"ip-address":"192.0.2.12"
}
```
**Response:**
```
Status: 200 OK
```
```
{
"uid": "9a8595e2-5791-487c-9dc4-45d3dbfea95e",
"folder": {"uid": "5abe7131-5821-4ee9-90b7-70cccef264d4","name": "/Global Objects"},
"domain": {"domain-type": "local domain","uid": "41e821a0-3720-11e3-aa6e-0800200c9fde","name": "SMC User"},
"meta-info": {"lock": "unlocked","validation-state": "ok","read-only": false,"last-modify-time": {"posix": 1430913372359,"iso-8601": "2015-05-06T14:56+0300"},
"last-modifier": "aa","creation-time": {"posix": 1430913372359,"iso-8601": "2015-05-06T14:56+0300"},"creator": "aa"},
"tags": [ ],
"name": "MyHost",
"comments": "",
"color": "black",
"icon": "Objects/host",
"groups": [ ],
"nat-settings": {"auto-rule": false},
"ipv4-address": "192.0.2.12",
"ipv6-address": ""
}
```
### A Sample Python script that use the web-service APIs:
```
import requests, json
def api_call(ip_addr, port, command, json_payload, sid):
url = 'https://' + ip_addr + ':' + port + '/web_api/' + command
if sid == '':
request_headers = {'Content-Type' : 'application/json'}
else:
request_headers = {'Content-Type' : 'application/json', 'X-chkp-sid' : sid}
r = requests.post(url,data=json.dumps(json_payload), headers=request_headers)
return r.json()
def login(user,password):
payload = {'user':user, 'password' : password}
response = api_call('192.168.65.2', 443, 'login',payload, '')
return response["sid"]
sid = login('my_username','secret')
print("session id: " + sid)
new_host_data = {'name':'new host name', 'ip-address':'192.168.1.1'}
new_host_result = api_call('192.168.65.2', 443,'add-host', new_host_data ,sid)
print(json.dumps(new_host_result))
publish_result = api_call('192.168.65.2', 443,"publish", {},sid)
print("publish result: " + json.dumps(publish_result))
logout_result = api_call('192.168.65.2', 443,"logout", {},sid)
print("logout result: " + json.dumps(logout_result))
```