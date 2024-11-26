- End user applications, we choose the protocols based on the programs that we are running.
- Requires and accesses services provided by [[Transport Layer]] to determine how conversations between entities occur.
- Apps and services communicate with lower layers through [[TCP]] and [[UDP]] ports. 

When choosing the application architecture there are two main models to choose from:
- Client- server architecture
    - Server is constantly running so can connect at any time e.g. web browser
- P2P architecture: very good for scalability.

Sockets allow for sending and receiving of messages from hosts to clients.

A socket is the interface between the application layer and the transport layer within a host, also referred to as the API (Application Programming Interface) between application and network.

### Building applications
Programming languages that allows network application development need to provide an API that allows code to be written that access the protocols and connects the layers.

The two main functions of a socket are:
1. Listen for incoming requests.
2. Send data onto the network.

At the Application layer the protocols include Telnet, File Transfer Protocol (FTP), Simple Main Transport Protocol (SMTP) and Domain Name Service (DNS).
### HTTP:
- Stateless protocol
- Used to view web pages, and it also makes requests for specific web pages.
- URLs : unique identifiers combining the domain name, directory structure and file name. 
- Most common form of HTTP is 1.0 a simple request response

**Request formats:
- GET: Read a web page
- HEAD: Read page headers
- POST: Append web page
- PUT: Store web page
- DELETE: Remove web page
- TRACE: Echo incoming request
- CONNECT: Query options available for web page

**Status codes:
- 200- ok
- 300- redirects
- 400- client side errors
- 500- server side errors
