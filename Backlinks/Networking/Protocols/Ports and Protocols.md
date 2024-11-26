Common way to communicate between different devices, defining the format and order of the messages being exchanged. 

Physical ports - Connect wires to. 
Logical Ports (Socket) - Determines where traffic and data goes. 

**Groups of ports:
- Well known: 0-1023, used for common protocols. 
- Registered: 1024-19151, proprietary applications, usually random. 
- Dynamic / Private: 49152 onwards. 

**Secure ports:**
- 22 - SSH
- 23 - Telnet - remote login service, unencrypted text messaged
- 25 - SMTP (Mail protocol using POP and IMAP)
- 53 - DNS
- 80 - HTTP
- 143 - IMAP
- 443- HTTPS - [[TLS]]
- 853 - DNS - [[TLS]]