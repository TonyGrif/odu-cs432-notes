# The Web
The Web is a system of interlinked hypertext documents accessed over [[#The Internet | the Internet]] using [[#Hypertext Transfer Protocol | HTTP(S)]].

The web is also an information space in which the items of interest (resources) are identified by global identifiers called [[#URI | Uniform Resource Identifiers (URI)]].
## Hypertext Transfer Protocol
Set of rules that govern communication between clients and servers.
### Requests
Requests are made by the client to the server to access or manipulate a resource on the server.
#### Format
* Request Line.
* Optional Header Lines.
* Body (optional).
#### Making Requests
Web servers can be communicated to with HTTP through various tools.
##### [Curl](https://curl.se/)
* Request only the HTTP response headers: `--head` or `-I` flags.
* Get body: `curl URL`.
* Get headers and body: `-i` flag.
##### [Wget](https://www.gnu.org/software/wget/)
* Save the body as a local file: `wget URL`.
    * This will default be `index.html`.
##### Raw Requests with Telnet
* Type in the status line.
    * Make request (get, post, ect).
    * Set host: `Host: www.`.
    * Set connection.
    * Blank line to get response.
* Does not work with HTTPS.
### Responses
Responses are sent from the server to the client to provide the client with the resource or send an error.
#### Format
* Status Line.
* Optional Header Lines.
* Request Object, Error Message(s), etc.
#### Response Codes
* 1xx: informational, request received, continuing process.
* 2xx: success.
* 3xx: redirection.
* 4xx: client error, request contains bad syntax/cannot be fulfilled.
* 5xx: server error, server failed to fulfill valid request.
## URI
Uniform Resource Identifiers used to identify resources. Representations of the resource are returned to the client.
### URx
* URI: string of characters used to identify a name or resources on [[#The Internet | the Internet]].
* URL: where to find the resource.
* URN: name of the resource.
# The Internet
The Internet is a global system of interconnected computer networks that use [[#Internet Protocol Suite | TCP and IP]] and [[#Domain Name System (DNS) | DNS]] to serve users.
## Internet Protocol Suite
* IP: Internet Protocol, directs packets to specific computer using IP address.
* TCP: Transmission Control Protocol, directs packets to specific app on computer using port numbers. Common port numbers:
    * 22: Ssh
    * 23: Telenet
    * 25: Email
    * 80: Web (HTTP)
    * 443: Web (HTTPS)
## Domain Name System (DNS)
Hierarchical look-up service that converts given host-name to equivalent IP address. DNS servers contact parent servers for missing entries and authoritative name servers are responsible for specific domains.