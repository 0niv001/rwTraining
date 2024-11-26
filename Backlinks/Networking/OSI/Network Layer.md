Gets packets from the source to the destination, which might require hopping between many routers. 

Responsible for host-to-host data delivery, involving network layer addressing, fragmentation, [[Routing]] and interworking.

Even though there are different link technologies, addresses and protocols, the transport layer is comprised of a numeric addressing scheme.

*Key roles:
- Forwarding packets from sending to receiving host.
- Encapsulating packets into diagrams, or delivering them to the transport layer.

*Main functions:
- Forwarding: Moving packets from input to right output, router local action.
- [[Routing]]

**Interplay between routing and forwarding**

[[Router]] establish virtual connections that allow the sender and receiver.

Packet switched networks providing connectionless, unreliable service are called datagram networks, which do not have session states in the network core.

Routers treat datagrams separately and their behaviour is statistical, meaning that different datagrams can take different paths to arrive at the same destination.

In the Internet layer, Internet Control Message Protocol (ICMP) is used to determine the health of a network or link. Used by [[Ping]]and [[Traceroute]]