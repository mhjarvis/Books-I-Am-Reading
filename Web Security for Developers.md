<h1 style="text-align:center"><strong>Web Security for Developers</strong></h1>

## <strong>1. Let's Hack a Website</strong>
Basically, use Kali. 

## <strong>2. How The Internet Works</strong>

### <strong>The Internet Protocol Suite:</strong>
TCP, UDP, IPs, and DNS reviews. 

### <strong>Application Layer Protocols</strong>
Application Layer:      DNS FTP HTTP IMAP POP SMTP SSH XMPP
Transport Layer:        TCP UDP
Internet Layer:         IPv4 IPv6
Network Layer:          ARP MAC NDP OSPF PPP

While TCP and UDP help transport information between systems, to interpret the data that is sent, systems use application layer protocols. HTTP is used to transport web pages to web browsers. Resource requests are created by a user to a web server, who respond with those requests (or an error code). Most of these responses are sent plain text, but they can be compressed and encrypted. HTTP requests sent by a browser consist of the following elements:

* Method - known as a verb, describe the action that the user agent wants the server to perform (GET, POST, PUT, PATCH, DELETE). 
* Universal Resource Locator (URL) - the resource being manipulated or fetched.
* Headers - supplies metadata such as the type of content the user is expecting or whether it accepts compressed responses.
* Body - (optional) contains extra data that needs to be sent to the server.

Some of the methods:

    GET - requests to fetch resources
    POST - sends information to servers
    HEAD - same as GET, but without a body
    CONNECT - initiates two-way communications.
    OPTIONS - asks what methods are supported by the resource
    TRACE - contains exact copy of the original HTTP request

HTTP responses usually include protocol description (HTTP/1.1), a three-digit status code (200, 404), a status message (OK), headers providing metadata, and a body (data requested). 

### <strong>Stateful Connections</strong>
Because there is constant exchange of information between user and server, there is a need for stateful connections - handshakes that allow parties to continue to communicate. This can be achieved via a HTTP session. Sessions are commonly tracked by the server sending back a ```Set-Cookie``` header in its initial HTTP response. The cookie that is stored contains some text pertaining to that web domain. Information from the cookie can then be used to uniquely identify the user and establish an HTTP session. 

### <strong>Encryption</strong>
TLS which leads to HTTPS. Requires TLS handshake, where both parties agree on an encryption method (cipher) and exchange encryption keys.

## <strong>3. How Browsers Work</strong>

### <strong>Web Page Rendering</strong>
The ```rendering pipeline``` is the software component responsible for transforming a web page's HTML into something you can view. When  HTTP response is received, the browser parses the body of the response into a Document Object Model (DOM). Styling is applied to the DOM. Once complete, the webpage is 'drawn' onscreen. JavaScript is also loaded and executed as it is encountered. 

JavaScript code will be executed when rendering a webpage, so ensure to use the ```defer``` attribute. Otherwise, reference errors will occur.

Because of security concerns, most modern JavaScript code is executed within a sandbox. 

## <strong>4. How Web Servers Work</strong>

### <strong>Static and Dynamic Resources</strong>
Web servers serve two types of content in response to HTTP requests:

    Static resource - an HTML file, image file, or other type of file that the web server returns unaltered in HTTP responses. 
    Dynamic resource - code, a script, or a template that the web server executes or interprets in response to an HTTP request.

### <strong>Static Resources</strong>
A static response will show in the url with the ```.html``` suffix, indicating that the file corresponds to an HTML file on the server. 

    Cloud Delivery Network (CDN) - used to improve delivery speeds of static files by storing duplicate copies of resources in data centers around the world. Can be the cause of security issues as you allow a third party to serve content under your security certificate.

    Content Management Systems (CMS) - provide tools to build websites with little to no technical knowledge. Sites created this way can be more secure because a company is behind the code, but if individual users don't patch their sites, they leave themselves open for vulnerabilities.

### <strong>Static Resources</strong>
Static resources implement the use of a database. This makes it easier to add new products by adding new rows to a database and implementing content via JavaScript. The same goes for websites like Google, where users experience is different for each individual as it is dynamically loaded.

### <strong>SQL Databases</strong>
Structured Query Language (SQL) databases are relational, meaning they store data in one or more tables that relate to each other. Tables relate to each other via ```keys```. Usually, each row in a table has a unique numeric ```primary key```, and tables can refer to each other's rows via ```foreign keys```. 

### <strong>NoSQL Databases</strong>
SQL databases are often bottlenecks for performance. Hence, the emergence of NoSQL, which sacrifices data integrity (some) for scalability. NoSQL databases are often schema-less, storing data in key-value form (or in JSON). 

## <strong>5. How Programmers Work</strong>
The 5 phases of SDLC: Design and Analysis, Writing Code, Pre-release Testing, the Release Process, and Post-release testing and observation.

## <strong>6. Injection Attacks</strong>
Injection attacks are those where an attacker injects external code into an application in an effort to take control of the application or read sensitive data. This is done by malicious HTTP requests. 

### <strong>SQL Injection</strong>
SQL Injection uses data queries to a database in an insecure fashion.

### <strong></strong>
Command Injection attacks uses code that makes insecure calls to operating system functions.

### <strong></strong>
Remote Code Execution allow attackers to run exploits inside the web server process itself. 

File upload functions often enable command injections if they write uploaded files to disk with executable privileges. Write uploads to a third-party system or to a disk with appropriate permissions. 





### <strong></strong>
### <strong></strong>
### <strong></strong>
### <strong></strong>
