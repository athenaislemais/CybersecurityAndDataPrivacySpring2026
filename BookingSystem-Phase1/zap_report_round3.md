# ZAP by Checkmarx Scanning Report

ZAP by [Checkmarx](https://checkmarx.com/).


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 1 |
| Medium | 2 |
| Low | 0 |
| Informational | 2 |




## Insights

| Level | Reason | Site | Description | Statistic |
| --- | --- | --- | --- | --- |
| High | Exceeded High |  | Percentage of memory used | 98    |
| Low | Warning |  | ZAP errors logged - see the zap.log file for details | 59    |
| Low | Warning |  | ZAP warnings logged - see the zap.log file for details | 1    |
| Low | Exceeded High | http://localhost:8003 | Percentage of responses with status code 4xx | 50 % |
| Info | Informational | http://localhost:8003 | Percentage of responses with status code 2xx | 35 % |
| Info | Informational | http://localhost:8003 | Percentage of responses with status code 3xx | 9 % |
| Info | Exceeded Low | http://localhost:8003 | Percentage of responses with status code 5xx | 7 % |
| Info | Informational | http://localhost:8003 | Percentage of endpoints with content type application/javascript | 20 % |
| Info | Informational | http://localhost:8003 | Percentage of endpoints with content type text/css | 6 % |
| Info | Informational | http://localhost:8003 | Percentage of endpoints with content type text/html | 26 % |
| Info | Informational | http://localhost:8003 | Percentage of endpoints with content type text/plain | 33 % |
| Info | Informational | http://localhost:8003 | Percentage of endpoints with method GET | 86 % |
| Info | Informational | http://localhost:8003 | Percentage of endpoints with method POST | 13 % |
| Info | Informational | http://localhost:8003 | Count of total endpoints | 15    |




## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- |
| SQL Injection | High | 16 |
| Absence of Anti-CSRF Tokens | Medium | 1 |
| Format String Error | Medium | 16 |
| Authentication Request Identified | Informational | 1 |
| User Agent Fuzzer | Informational | Systemic |




## Alert Detail



### [ SQL Injection ](https://www.zaproxy.org/docs/alerts/40018/)



##### High (Low)

### Description

SQL injection may be possible.

* URL: http://localhost:8003
  * Node Name: `http://localhost:8003`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8003'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8003/
  * Node Name: `http://localhost:8003/`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8003'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8003/login
  * Node Name: `http://localhost:8003/login`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8003'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8003/register
  * Node Name: `http://localhost:8003/register`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8003'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8003/reservation
  * Node Name: `http://localhost:8003/reservation`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8003'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8003/resources
  * Node Name: `http://localhost:8003/resources`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8003'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8003/robots.txt
  * Node Name: `http://localhost:8003/robots.txt`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8003'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8003/sitemap.xml
  * Node Name: `http://localhost:8003/sitemap.xml`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8003'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8003/static
  * Node Name: `http://localhost:8003/static`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8003'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8003/static/footer.js
  * Node Name: `http://localhost:8003/static/footer.js`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8003'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8003/static/index.js
  * Node Name: `http://localhost:8003/static/index.js`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8003'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8003/static/status.js
  * Node Name: `http://localhost:8003/static/status.js`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8003'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8003/static/tailwind.css
  * Node Name: `http://localhost:8003/static/tailwind.css`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8003'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8003/status.html%3Fmessage=%253Cstrong%253EValidation%2520Error(s&29%253A%253C%252Fstrong%253E%253Cbr%253EInvalid%2520email%2520or%2520password!&status=failed
  * Node Name: `http://localhost:8003/status.html (message,status)`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8003'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8003/login
  * Node Name: `http://localhost:8003/login ()(csrf_token,password,username)`
  * Method: `POST`
  * Parameter: `host`
  * Attack: `localhost:8003'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8003/register
  * Node Name: `http://localhost:8003/register ()(birthdate,password,role,username)`
  * Method: `POST`
  * Parameter: `host`
  * Attack: `localhost:8003'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``


Instances: 16

### Solution

Do not trust client side input, even if there is client side validation in place.
In general, type check all data on the server side.
If the application uses JDBC, use PreparedStatement or CallableStatement, with parameters passed by '?'
If the application uses ASP, use ADO Command Objects with strong type checking and parameterized queries.
If database Stored Procedures can be used, use them.
Do *not* concatenate strings into queries in the stored procedure, or use 'exec', 'exec immediate', or equivalent functionality!
Do not create dynamic SQL queries using simple string concatenation.
Escape all data received from the client.
Apply an 'allow list' of allowed characters, or a 'deny list' of disallowed characters in user input.
Apply the principle of least privilege by using the least privileged database user possible.
In particular, avoid using the 'sa' or 'db-owner' database users. This does not eliminate SQL injection, but minimizes its impact.
Grant the minimum database access that is necessary for the application.

### Reference


* [ https://cheatsheetseries.owasp.org/cheatsheets/SQL_Injection_Prevention_Cheat_Sheet.html ](https://cheatsheetseries.owasp.org/cheatsheets/SQL_Injection_Prevention_Cheat_Sheet.html)


#### CWE Id: [ 89 ](https://cwe.mitre.org/data/definitions/89.html)


#### WASC Id: 19

#### Source ID: 1

### [ Absence of Anti-CSRF Tokens ](https://www.zaproxy.org/docs/alerts/10202/)



##### Medium (Low)

### Description

No Anti-CSRF tokens were found in a HTML submission form.
A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.

CSRF attacks are effective in a number of situations, including:
    * The victim has an active session on the target site.
    * The victim is authenticated via HTTP auth on the target site.
    * The victim is on the same local network as the target site.

CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.

* URL: http://localhost:8003/register
  * Node Name: `http://localhost:8003/register`
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `<form action="/register" method="POST">`
  * Other Info: `No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF, _token, _csrf_token, _csrfToken] was found in the following HTML form: [Form 1: "birthdate" "password" "username" ].`


Instances: 1

### Solution

Phase: Architecture and Design
Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.
For example, use anti-CSRF packages such as the OWASP CSRFGuard.

Phase: Implementation
Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.

Phase: Architecture and Design
Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).
Note that this can be bypassed using XSS.

Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.
Note that this can be bypassed using XSS.

Use the ESAPI Session Management control.
This control includes a component for CSRF.

Do not use the GET method for any request that triggers a state change.

Phase: Implementation
Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.

### Reference


* [ https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html ](https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html)
* [ https://cwe.mitre.org/data/definitions/352.html ](https://cwe.mitre.org/data/definitions/352.html)


#### CWE Id: [ 352 ](https://cwe.mitre.org/data/definitions/352.html)


#### WASC Id: 9

#### Source ID: 3

### [ Format String Error ](https://www.zaproxy.org/docs/alerts/30002/)



##### Medium (Medium)

### Description

A Format String error occurs when the submitted data of an input string is evaluated as a command by the application.

* URL: http://localhost:8003
  * Node Name: `http://localhost:8003`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `ZAP%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s
`
  * Evidence: ``
  * Other Info: `Potential Format String Error. The script closed the connection on a /%s.`
* URL: http://localhost:8003/
  * Node Name: `http://localhost:8003/`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `ZAP%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s
`
  * Evidence: ``
  * Other Info: `Potential Format String Error. The script closed the connection on a /%s.`
* URL: http://localhost:8003/login
  * Node Name: `http://localhost:8003/login`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `ZAP%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s
`
  * Evidence: ``
  * Other Info: `Potential Format String Error. The script closed the connection on a /%s.`
* URL: http://localhost:8003/register
  * Node Name: `http://localhost:8003/register`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `ZAP%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s
`
  * Evidence: ``
  * Other Info: `Potential Format String Error. The script closed the connection on a /%s.`
* URL: http://localhost:8003/reservation
  * Node Name: `http://localhost:8003/reservation`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `ZAP%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s
`
  * Evidence: ``
  * Other Info: `Potential Format String Error. The script closed the connection on a /%s.`
* URL: http://localhost:8003/resources
  * Node Name: `http://localhost:8003/resources`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `ZAP%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s
`
  * Evidence: ``
  * Other Info: `Potential Format String Error. The script closed the connection on a /%s.`
* URL: http://localhost:8003/robots.txt
  * Node Name: `http://localhost:8003/robots.txt`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `ZAP%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s
`
  * Evidence: ``
  * Other Info: `Potential Format String Error. The script closed the connection on a /%s.`
* URL: http://localhost:8003/sitemap.xml
  * Node Name: `http://localhost:8003/sitemap.xml`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `ZAP%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s
`
  * Evidence: ``
  * Other Info: `Potential Format String Error. The script closed the connection on a /%s.`
* URL: http://localhost:8003/static
  * Node Name: `http://localhost:8003/static`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `ZAP%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s
`
  * Evidence: ``
  * Other Info: `Potential Format String Error. The script closed the connection on a /%s.`
* URL: http://localhost:8003/static/footer.js
  * Node Name: `http://localhost:8003/static/footer.js`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `ZAP%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s
`
  * Evidence: ``
  * Other Info: `Potential Format String Error. The script closed the connection on a /%s.`
* URL: http://localhost:8003/static/index.js
  * Node Name: `http://localhost:8003/static/index.js`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `ZAP%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s
`
  * Evidence: ``
  * Other Info: `Potential Format String Error. The script closed the connection on a /%s.`
* URL: http://localhost:8003/static/status.js
  * Node Name: `http://localhost:8003/static/status.js`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `ZAP%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s
`
  * Evidence: ``
  * Other Info: `Potential Format String Error. The script closed the connection on a /%s.`
* URL: http://localhost:8003/static/tailwind.css
  * Node Name: `http://localhost:8003/static/tailwind.css`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `ZAP%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s
`
  * Evidence: ``
  * Other Info: `Potential Format String Error. The script closed the connection on a /%s.`
* URL: http://localhost:8003/status.html%3Fmessage=%253Cstrong%253EValidation%2520Error(s&29%253A%253C%252Fstrong%253E%253Cbr%253EInvalid%2520email%2520or%2520password!&status=failed
  * Node Name: `http://localhost:8003/status.html (message,status)`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `ZAP%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s
`
  * Evidence: ``
  * Other Info: `Potential Format String Error. The script closed the connection on a /%s.`
* URL: http://localhost:8003/login
  * Node Name: `http://localhost:8003/login ()(csrf_token,password,username)`
  * Method: `POST`
  * Parameter: `host`
  * Attack: `ZAP%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s
`
  * Evidence: ``
  * Other Info: `Potential Format String Error. The script closed the connection on a /%s.`
* URL: http://localhost:8003/register
  * Node Name: `http://localhost:8003/register ()(birthdate,password,role,username)`
  * Method: `POST`
  * Parameter: `host`
  * Attack: `ZAP%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s
`
  * Evidence: ``
  * Other Info: `Potential Format String Error. The script closed the connection on a /%s.`


Instances: 16

### Solution

Rewrite the background program using proper deletion of bad character strings. This will require a recompile of the background executable.

### Reference


* [ https://owasp.org/www-community/attacks/Format_string_attack ](https://owasp.org/www-community/attacks/Format_string_attack)


#### CWE Id: [ 134 ](https://cwe.mitre.org/data/definitions/134.html)


#### WASC Id: 6

#### Source ID: 1

### [ Authentication Request Identified ](https://www.zaproxy.org/docs/alerts/10111/)



##### Informational (High)

### Description

The given request has been identified as an authentication request. The 'Other Info' field contains a set of key=value lines which identify any relevant fields. If the request is in a context which has an Authentication Method set to "Auto-Detect" then this rule will change the authentication to match the request identified.

* URL: http://localhost:8003/login
  * Node Name: `http://localhost:8003/login ()(csrf_token,password,username)`
  * Method: `POST`
  * Parameter: `username`
  * Attack: ``
  * Evidence: `password`
  * Other Info: `userParam=username
userValue=foo-bar@example.com
passwordParam=password
referer=http://localhost:8003/login
csrfToken=csrf_token`


Instances: 1

### Solution

This is an informational alert rather than a vulnerability and so there is nothing to fix.

### Reference


* [ https://www.zaproxy.org/docs/desktop/addons/authentication-helper/auth-req-id/ ](https://www.zaproxy.org/docs/desktop/addons/authentication-helper/auth-req-id/)



#### Source ID: 3

### [ User Agent Fuzzer ](https://www.zaproxy.org/docs/alerts/10104/)



##### Informational (Medium)

### Description

Check for differences in response based on fuzzed User Agent (eg. mobile sites, access as a Search Engine Crawler). Compares the response statuscode and the hashcode of the response body with the original response.

* URL: http://localhost:8003/login
  * Node Name: `http://localhost:8003/login ()(csrf_token,password,username)`
  * Method: `POST`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/4.0 (compatible; MSIE 7.0; Windows NT 6.0)`
  * Evidence: ``
  * Other Info: ``
* URL: http://localhost:8003/login
  * Node Name: `http://localhost:8003/login ()(csrf_token,password,username)`
  * Method: `POST`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/4.0 (compatible; MSIE 8.0; Windows NT 6.1)`
  * Evidence: ``
  * Other Info: ``
* URL: http://localhost:8003/register
  * Node Name: `http://localhost:8003/register ()(birthdate,password,role,username)`
  * Method: `POST`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)`
  * Evidence: ``
  * Other Info: ``
* URL: http://localhost:8003/register
  * Node Name: `http://localhost:8003/register ()(birthdate,password,role,username)`
  * Method: `POST`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/4.0 (compatible; MSIE 7.0; Windows NT 6.0)`
  * Evidence: ``
  * Other Info: ``
* URL: http://localhost:8003/register
  * Node Name: `http://localhost:8003/register ()(birthdate,password,role,username)`
  * Method: `POST`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/4.0 (compatible; MSIE 8.0; Windows NT 6.1)`
  * Evidence: ``
  * Other Info: ``

Instances: Systemic


### Solution



### Reference


* [ https://owasp.org/wstg ](https://owasp.org/wstg)



#### Source ID: 1


