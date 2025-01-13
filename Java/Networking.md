Socket and ServerSocket Class - Create and close sockets, send and receive data. 

Socket - one endpoint of 2 way comms between programs running on a network.

**Reading**
DataInputStream and output classes to read and write data over a network.

**Client server**
Model for distributed computing, server and clients. 
Can use Java to build servers. 

*Creating server*
Create serverSocket object, connect it to port. 
Create Socket object for every client that connects to the server. 
Use the same socket on both ends

*Creating client application*
Create Socket object and connect to server. 


Datagram sockets - Connectionless, do not establish reliable connection. UDP÷