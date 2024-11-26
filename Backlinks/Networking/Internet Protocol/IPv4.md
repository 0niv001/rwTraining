32bit address space. 

Need to use [[NAT]]for [[Private IP]]

v4 Addresses are expressed as 4 octets separated by a dot, each octet can have a value between 0 and 255, but 0 is the network itself and 255 is usually left out for broadcasts.

Each address is divided into two parts:
1. Network number: assigned by external organisation represents the organisation’s network.
2. Host: represents the network interface within the network.

To make network admin simpler, networks are divided into subnets, as these can’t be distinguished with the same addressing scheme, a subnet mask is used to define the part of the address used for the subnet, which is the decimal address we are familiar with. 

v4 allowed for the creation of the private address groups; allowing every LAN in every SOHO (small office, home office) to use addresses such as [192.168.2.xxx](http://192.168.2.xxx/) for its internal network addresses, without fear that some other system can intercept traffic on their LAN.


First octet of 127 is reserved for computer’s loopback address. Usually 127.0.0.1dress

Special IP addresses 
127.0.0.0 - Loopback address. 
169.254.0.0 - Link local. 
192.0.0.0 - Used for private purposes. 
224.0.0.0 - Multicast. 