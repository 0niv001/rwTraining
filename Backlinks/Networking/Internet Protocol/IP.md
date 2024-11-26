Unique logical address given to devices connected to a network, used to identify a network and the hosts on it. 

It is a data oriented and best effort protocol, meaning it does not guarantee delivery or correctness of data. Issue addressed by [[TCP]]

It allows to keep the connection when the physical device is swapped with new hardware. 

**Address Formats:**
- [[IPv4]]
- [[IPv6]]

**Types of address:**
- [[Public IP]]
- [[Private IP]]

**IP address assignment:**
- Static IP: Manual assignment
- Dynamic IP: Assigned using [[DHCP]]

In classful addressing IP address is divided into class type, network number and host number

In private IP addressing, hosts on a LAN that are not visible on public internet are given private addresses.

**ARP (Address Resolution Protocol)**
A method for translating between the internet layer and the network layer address. 
Between IP and [[MAC]] 

The steps of ARP translation using [[TCP]]/IP are:

1. Check cache to see if it knows mappings between IP address and physical address
2. ARP broadcast a request to the local network if there is no match, which is then received by every computer and router that is connected to the host.
3. If matching IP exists it sends the MAC address back, and the translation is saved in the cache
4. If the router finds that the IP is outside the local network it sends back its MAC address so that the datagram can be forwarded to it.