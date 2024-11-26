Family of related protocols.
Allows frame format to stay the same across different speeds, allowing systems to be used in parallel. 

Modern LANs are laid out in star and extended star topologies using Ethernet [[Switches]]

Defines the way the data is formatted over wire to ensure different devices can communicate on the same cable. 

**CSMA / CD**
- Rules that determine how network devices respond when two devices try to use a channel at the same time. 
- Used to monitor traffic on the line in that sub-network. 
- *Carrier Sense:* network listens out for traffic to establish if data is being transmitted, if not then it can send data. 
- *Multiple Access:* Prevents 2+ devices from sending data at the same time. 
- *Collision Detection:* If there is a collision one device waits before trying to send a packet off. 

As networks grow, there will be more and more collisions, so the networks will have to be broken down into smaller [[Subnet]]