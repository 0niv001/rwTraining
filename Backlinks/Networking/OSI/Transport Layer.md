Direct data to the right socket from network , providing comms between endpoints. 

*Roles:
- Break down data into packets called segments. 
- Add header to segments. 
- Pass segments to the [[Network Layer]]
- Reliable data transfer: Guarantees that all packets will arrive at the destination, the socket manages everything. 
- Throughput guarantees: Network traffic volume is always in flux, some applications are bandwidth sensitive and so a throughput guarantee might be best to use
- Timing guarantees: Defines a maximum amount of time within which communication is sent ensures timeliness
- Security: Can select protocols like [[Encryption]] and [[Authentication]]

Two main types of connection:
1. [[UDP]]
2. [[TCP]]

Both [[TCP]] and [[UDP]] run on top of the [[IP]] layer