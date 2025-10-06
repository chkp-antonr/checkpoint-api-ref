---
title: Tips & Best Practices
source_html: C:\_Labs\Dev\checkpoint-api-ref-py\out\html\tips_best_practices.html
generatedAt: '2025-10-05T18:45:55.726953+00:00'
---

# Tips & Best Practices
This section describes best practices for working with the Management API.
Here you can learn the best way to write API scripts, and how to overcome the performance impact of massive usage of the API.
### Best Practice
Use one or more dedicated users for API operations to make sure minimum permissions are granted.
### Scripting Tips
* To get scripting examples, refer to Check Point's [Github account](https://github.com/checkpointsw) and posts by API team members on [CheckMates](https://community.checkpoint.com/community/developers).
* To kick-start your scripting, use the official Check Point SDKs (in Java, Python, and C#), which are published in the Check Point [github](https://github.com/search?q=org%3ACheckPointSW+sdk&unscoped_q=sdk) account. No need to develop your own SDKs.
* Store the session id in a variable as part of your script, and not in a file. The advantages of this approach are:
* No clean-up of the files required.
* When running the scripts multiple times, there is no possibility that the file containing the session ID will be accidentally overwritten.
* Use the --format json flag (or -f json) when using the mgmt\_cli. Use jq to filter and parse your results. This is much easier than using grep,sed,awk or tr.
**Example:**  Filter hosts with the color blue and output their name, uid and ip address to a csv file.
```
mgmt_cli show hosts details-level full -f json | jq -r '.objects[] | select(.color == "blue")| [.name, .uid , ."ipv4-address"] |@csv'
```
For more details and examples see this [post](https://community.checkpoint.com/t5/Developers-API-CLI/How-to-parse-JSON-output-from-R80-Management-API-with-JQ/m-p/14093?advanced=false&collapse_discussion=true&filter=location&location=forum-board:codehub&q=jq&search_type=thread)
* Perform Login at the beginning of the script and Logout at the end. See examples in the *'Performance Tips'* section below
* Specify the version as part of your commands to make sure future upgrades won't affect your scripts. Do it using the --version flag if you are using the CLI tool or add vX.X to the URL if you are using the Web-Services.
### Performance Tips
* Login to last published session (enter-last-published-session) when you don't need to make any changes or updates. For example, if all commands are of type "show". This is because login for reading and writing has more database overhead than a login for read-only and other publishes will not affect your session.
**Example 1**(mgmt\_cli)**:**
```
mgmt_cli login user "aa" password "aaaa" enter-last-published-session true -f json
```
**Example 2**(Web Services)**:**
```
POST {{server}}/login
Content-Type: application/json
{
"user" : "aa",
"password" : "aaaa"
"enter-last-published-session" : "true"
}
```
* When using the mgmt\_cli, reduce the number of logins and logouts to the minimum possible by using sessions, and working within one session..
* Using one session is faster. If you do not explicitly use a session ID (sid), then each command results in this set of operations: login, action, publish, and logout. All these extra operations cause a higher management and database overhead.
* Reducing the number of sessions helps you avoid reaching maximum allowed number of concurrent read/write sessions. The maximum is 100.
**Bad Practice Example (pseudo code):**
In this example, API call is being executed without an explicit session-id. This means that each time, four commands are being executed (login,add-host,publish and logout)
```
for i=0 to i<100 do:
mgmt_cli -r true add-host name hosts_list[i] ip-address ip_list[i]
```
**Good Practice Example (pseudo code):**
In this example, login is done just once. All changes are made in one session, and at the end of the session there is a publish and logout. This saves the overhead of managing multiple login and logout operations on the server.
```
session=`mgmt_cli -r true login --format json| jq -r '.sid'` //  login once and set session id (sid) into a variable
for i=0 to i<100  do:
mgmt_cli add-host name hosts_list[i] ip-address ip_list[i]  --session-id $session // use the session id for adding hosts in loop
mgmt_cli publish --session-id $session  // publish all changes in one session. Publish occur only once
mgmt_cli logout --session-id $session  // logout once
```
**Note-** If you have many hundreds of changes, it is best to avoid publishing once at the end of the session. Instead, publish a few times within your session. For example, publish every 100 changes. However, you only need to log in once at the beginning of the session, and log out at the end of the session.
* Starting from R81, login from a remote machine is limited to 3 logins per minute for each admin to a specific domain. Your scripts should catch the error below and try again later:
```
{
"code": "err_too_many_requests",
"message": "Too many requests in a given amount of time"
}
```
**Example (pseudo code):**
```
retries = 0
DO
wait for (2^retries) seconds
result = Do login operation.
IF result.is_success = true
retry = false
ELSE IF result.is_success = false
IF result.get_error_message = "Too many requests in a given amount of time"
retry = true
ELSE
Some other error occurred, stop calling the API.
retry = false
END IF
retries = retries + 1
WHILE (retry AND (retries < MAX_RETRIES))
```
* Take advantage of using the limit and details-level arguments as part of request to control the amount of data in the replies to the API calls.
* Take advantage of the show-changes command
* API calls that traverse the entire security management database result in high I/O and RAM rates. For example, exporting entire security policies and all objects that are referenced to them. Or, exporting all network objects, especially with large environments, or with repetitions of such exports.
If you use the security management APIs for constant export and import of data, consider using the automatic revisions that come with the R81.20 Management Platform. The show-changes API command receives start and end dates, or revisions UIDs, and returns the created, deleted and changed configuration objects.
It is more efficient to work with deltas rather than working on the entire security management configuration.
* To achieve optimum performance when either adding, updating, or deleting more than one object, use the following APIs:
* add-objects-batch
* set-objects-batch
* delete-objects-batch