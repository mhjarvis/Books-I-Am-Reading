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

HTTP responses usuallly includea protocol description (HTTP/1.1), a three-digit status code (200, 404), a status message (OK), headers providing metadata, and a body (data requested). 

### <strong>Stateful Connections</strong>
Because there is constant exchange of information between user and server, there is a need for stateful connections - handshakes that allow parties to continue to communicate. This can be achieved via a HTTP session. Sessions are commonly tracked by the server sending back a ```Set-Cookie``` header in its initial HTTP response. The cookie that is stored contains some text pertaining to that web domain. Information from the cookie can then be used to uniquely identify the user and establish an HTTP session. 

### <strong>Encryption</strong>
TLS which leads to HTTPS. Requires TLS handshake, where both parties agree on an encryption method (cipher) and exchange encryption keys.

