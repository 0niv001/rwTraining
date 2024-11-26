**Packet and Circuit switching**

Messages sent between endpoints are broken down into chunks known as packets and then reassembled at the other end.

Going from one end to another can involve many nodes in between, routers and link layer switches are responsible for routing them.

Store and forward transmission is used to make sure that whole packets are received before they are forwarded. To make this work packets have a buffer called output queue.

If there is not enough space in the buffer packets may be dropped and lost.

To make sure the packets are received by the right recipient [[IP]] addresses are checked at each node.

Routing protocols determine which nodes packets will go through to arrive at their destination, since nodes are constantly going on and off line, as well as having different levels of business.

**Routing Protocols**
- Router Information Protocol (RIP)
- Open shortest path first (OSPF)
- Interior gateway routing protocol (IGRP)
- Enhanced IGRP
- Border gateway protocol (BGP)
- Intermediate system to intermediate system (IS-IS)
- Constrained Shortest Path First (CSPF)

Routing protocols can be evaluated by looking at the minimum hops and least cost routes. 