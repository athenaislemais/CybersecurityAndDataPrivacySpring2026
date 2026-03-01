# zap_report_round4

ZAP by [Checkmarx](https://checkmarx.com/).


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 1 |
| Medium | 1 |
| Low | 0 |
| Informational | 4 |




## Insights

| Level | Reason | Site | Description | Statistic |
| --- | --- | --- | --- | --- |
| High | Exceeded High |  | Percentage of memory used | 97    |
| Low | Warning |  | ZAP errors logged - see the zap.log file for details | 146    |
| Low | Warning |  | ZAP warnings logged - see the zap.log file for details | 216    |
| Info | Informational |  | Percentage of network failures | 1 % |
| Info | Informational | http://localhost:8004 | Percentage of responses with status code 2xx | 43 % |
| Info | Informational | http://localhost:8004 | Percentage of responses with status code 3xx | 14 % |
| Info | Exceeded Low | http://localhost:8004 | Percentage of responses with status code 4xx | 36 % |
| Info | Exceeded Low | http://localhost:8004 | Percentage of responses with status code 5xx | 5 % |
| Info | Informational | http://localhost:8004 | Percentage of endpoints with content type application/javascript | 17 % |
| Info | Informational | http://localhost:8004 | Percentage of endpoints with content type image/png | 4 % |
| Info | Informational | http://localhost:8004 | Percentage of endpoints with content type text/css | 4 % |
| Info | Informational | http://localhost:8004 | Percentage of endpoints with content type text/html | 26 % |
| Info | Informational | http://localhost:8004 | Percentage of endpoints with content type text/plain | 30 % |
| Info | Informational | http://localhost:8004 | Percentage of endpoints with method GET | 86 % |
| Info | Informational | http://localhost:8004 | Percentage of endpoints with method POST | 13 % |
| Info | Informational | http://localhost:8004 | Count of total endpoints | 23    |
| Info | Informational | http://localhost:8004 | Percentage of slow responses | 2 % |
| Info | Informational | https://archive.mozilla.org | Percentage of responses with status code 2xx | 100 % |
| Info | Informational | https://archive.mozilla.org | Percentage of endpoints with content type application/x-xpinstall | 100 % |
| Info | Informational | https://archive.mozilla.org | Percentage of endpoints with method GET | 100 % |
| Info | Informational | https://archive.mozilla.org | Count of total endpoints | 2    |
| Info | Informational | https://archive.mozilla.org | Percentage of slow responses | 100 % |
| Info | Informational | https://firefox-settings-attachments.cdn.mozilla.net | Percentage of endpoints with content type text/plain | 100 % |
| Info | Informational | https://firefox-settings-attachments.cdn.mozilla.net | Percentage of endpoints with method GET | 100 % |
| Info | Informational | https://firefox-settings-attachments.cdn.mozilla.net | Count of total endpoints | 3    |
| Info | Informational | https://firefox.settings.services.mozilla.com | Percentage of endpoints with content type application/json | 100 % |
| Info | Informational | https://firefox.settings.services.mozilla.com | Percentage of endpoints with method GET | 100 % |
| Info | Informational | https://firefox.settings.services.mozilla.com | Count of total endpoints | 2    |




## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- |
| SQL Injection | High | 18 |
| Format String Error | Medium | 4 |
| Authentication Request Identified | Informational | 1 |
| Session Management Response Identified | Informational | 3 |
| Tech Detected - Tailwind CSS | Informational | 1 |
| User Agent Fuzzer | Informational | Systemic |




## Alert Detail



### [ SQL Injection ](https://www.zaproxy.org/docs/alerts/40018/)



##### High (Low)

### Description

SQL injection may be possible.

* URL: http://localhost:8004
  * Node Name: `http://localhost:8004`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8004'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8004/
  * Node Name: `http://localhost:8004/`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8004'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8004/login
  * Node Name: `http://localhost:8004/login`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8004'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8004/register
  * Node Name: `http://localhost:8004/register`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8004'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8004/reservation
  * Node Name: `http://localhost:8004/reservation`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8004'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8004/resources
  * Node Name: `http://localhost:8004/resources`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8004'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8004/robots.txt
  * Node Name: `http://localhost:8004/robots.txt`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8004'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8004/sitemap.xml
  * Node Name: `http://localhost:8004/sitemap.xml`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8004'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8004/static
  * Node Name: `http://localhost:8004/static`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8004'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8004/static/footer.js
  * Node Name: `http://localhost:8004/static/footer.js`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8004'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8004/static/index.js
  * Node Name: `http://localhost:8004/static/index.js`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8004'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8004/static/resourceForm.js
  * Node Name: `http://localhost:8004/static/resourceForm.js`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8004'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8004/static/status.js
  * Node Name: `http://localhost:8004/static/status.js`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8004'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8004/static/tailwind.css
  * Node Name: `http://localhost:8004/static/tailwind.css`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8004'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8004/status.html%3Fmessage=%253Cstrong%253EValidation%2520Error(s&29%253A%253C%252Fstrong%253E%253Cbr%253EInvalid%2520email%2520or%2520password!&status=failed
  * Node Name: `http://localhost:8004/status.html (message,status)`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `localhost:8004'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8004/login
  * Node Name: `http://localhost:8004/login ()(csrf_token,password,username)`
  * Method: `POST`
  * Parameter: `host`
  * Attack: `localhost:8004'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8004/register
  * Node Name: `http://localhost:8004/register ()(birthdate,csrf_token,password,role,username)`
  * Method: `POST`
  * Parameter: `host`
  * Attack: `localhost:8004'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``
* URL: http://localhost:8004/resources
  * Node Name: `http://localhost:8004/resources ()(csrf_token,resource_description,resource_id,resource_name)`
  * Method: `POST`
  * Parameter: `host`
  * Attack: `localhost:8004'`
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  * Other Info: ``


Instances: 18

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

### [ Format String Error ](https://www.zaproxy.org/docs/alerts/30002/)



##### Medium (Medium)

### Description

A Format String error occurs when the submitted data of an input string is evaluated as a command by the application.

* URL: http://localhost:8004/status.html%3Fmessage=%253Cstrong%253EValidation%2520Error(s&29%253A%253C%252Fstrong%253E%253Cbr%253EInvalid%2520email%2520or%2520password!&status=failed
  * Node Name: `http://localhost:8004/status.html (message,status)`
  * Method: `GET`
  * Parameter: `host`
  * Attack: `ZAP%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s
`
  * Evidence: ``
  * Other Info: `Potential Format String Error. The script closed the connection on a /%s.`
* URL: http://localhost:8004/login
  * Node Name: `http://localhost:8004/login ()(csrf_token,password,username)`
  * Method: `POST`
  * Parameter: `host`
  * Attack: `ZAP%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s
`
  * Evidence: ``
  * Other Info: `Potential Format String Error. The script closed the connection on a /%s.`
* URL: http://localhost:8004/register
  * Node Name: `http://localhost:8004/register ()(birthdate,csrf_token,password,role,username)`
  * Method: `POST`
  * Parameter: `host`
  * Attack: `ZAP%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s
`
  * Evidence: ``
  * Other Info: `Potential Format String Error. The script closed the connection on a /%s.`
* URL: http://localhost:8004/resources
  * Node Name: `http://localhost:8004/resources ()(csrf_token,resource_description,resource_id,resource_name)`
  * Method: `POST`
  * Parameter: `host`
  * Attack: `ZAP%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s%n%s
`
  * Evidence: ``
  * Other Info: `Potential Format String Error. The script closed the connection on a /%s.`


Instances: 4

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

* URL: http://localhost:8004/login
  * Node Name: `http://localhost:8004/login ()(csrf_token,password,username)`
  * Method: `POST`
  * Parameter: `username`
  * Attack: ``
  * Evidence: `password`
  * Other Info: `userParam=username
userValue=foo-bar@example.com
passwordParam=password
referer=http://localhost:8004/login
csrfToken=csrf_token`


Instances: 1

### Solution

This is an informational alert rather than a vulnerability and so there is nothing to fix.

### Reference


* [ https://www.zaproxy.org/docs/desktop/addons/authentication-helper/auth-req-id/ ](https://www.zaproxy.org/docs/desktop/addons/authentication-helper/auth-req-id/)



#### Source ID: 3

### [ Session Management Response Identified ](https://www.zaproxy.org/docs/alerts/10112/)



##### Informational (High)

### Description

The given response has been identified as containing a session management token. The 'Other Info' field contains a set of header tokens that can be used in the Header Based Session Management Method. If the request is in a context which has a Session Management Method set to "Auto-Detect" then this rule will change the session management to use the tokens identified.

* URL: http://localhost:8004/login
  * Node Name: `http://localhost:8004/login`
  * Method: `GET`
  * Parameter: `csrf_token`
  * Attack: ``
  * Evidence: `csrf_token`
  * Other Info: `cookie:csrf_token`
* URL: http://localhost:8004/register
  * Node Name: `http://localhost:8004/register`
  * Method: `GET`
  * Parameter: `csrf_token`
  * Attack: ``
  * Evidence: `csrf_token`
  * Other Info: `cookie:csrf_token`
* URL: http://localhost:8004/login
  * Node Name: `http://localhost:8004/login`
  * Method: `GET`
  * Parameter: `csrf_token`
  * Attack: ``
  * Evidence: `csrf_token`
  * Other Info: `cookie:csrf_token`


Instances: 3

### Solution

This is an informational alert rather than a vulnerability and so there is nothing to fix.

### Reference


* [ https://www.zaproxy.org/docs/desktop/addons/authentication-helper/session-mgmt-id/ ](https://www.zaproxy.org/docs/desktop/addons/authentication-helper/session-mgmt-id/)



#### Source ID: 3

### [ Tech Detected - Tailwind CSS ](https://www.zaproxy.org/docs/alerts/10004/)



##### Informational (Medium)

### Description

The following "UI frameworks" technology was identified: Tailwind CSS.
Described as:
Tailwind is a utility-first CSS framework for rapidly building custom user interfaces.

* URL: http://localhost:8004/static/tailwind.css
  * Node Name: `http://localhost:8004/static/tailwind.css`
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `--tw-border-opacity`
  * Other Info: ``


Instances: 1

### Solution



### Reference


* [ https://tailwindcss.com/ ](https://tailwindcss.com/)



#### WASC Id: 13

#### Source ID: 4

### [ User Agent Fuzzer ](https://www.zaproxy.org/docs/alerts/10104/)



##### Informational (Medium)

### Description

Check for differences in response based on fuzzed User Agent (eg. mobile sites, access as a Search Engine Crawler). Compares the response statuscode and the hashcode of the response body with the original response.

* URL: http://localhost:8004/login
  * Node Name: `http://localhost:8004/login`
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/4.0 (compatible; MSIE 8.0; Windows NT 6.1)`
  * Evidence: ``
  * Other Info: ``
* URL: http://localhost:8004/register
  * Node Name: `http://localhost:8004/register`
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/4.0 (compatible; MSIE 8.0; Windows NT 6.1)`
  * Evidence: ``
  * Other Info: ``
* URL: http://localhost:8004/login
  * Node Name: `http://localhost:8004/login ()(csrf_token,password,username)`
  * Method: `POST`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/4.0 (compatible; MSIE 8.0; Windows NT 6.1)`
  * Evidence: ``
  * Other Info: ``
* URL: http://localhost:8004/register
  * Node Name: `http://localhost:8004/register ()(birthdate,csrf_token,password,role,username)`
  * Method: `POST`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/4.0 (compatible; MSIE 8.0; Windows NT 6.1)`
  * Evidence: ``
  * Other Info: ``
* URL: http://localhost:8004/resources
  * Node Name: `http://localhost:8004/resources ()(csrf_token,resource_description,resource_id,resource_name)`
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


