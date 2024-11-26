128bit address space. Modern version addressing issues of v4:
- *Larger address field* so we won't run out of addresses. 
- *Better security:* mandates IPsec ensuring [[CIA]] of IP packets. 
- *Better service quality:* Helps services gain the right amount of bandwidth. 
- Simpler packet format allowing for easier processing. 
- Can be used in all networks making [[NAT]] redundant. 

Shown in groups of 4 digits, separated by : 
To read them we can get rid of the 0s at the start of each field

Some addresses are kept for special uses:
- ::1 is the loopback address
- range 2001:db8:: to 2001:db8:ffff:ffff:ffff:ffff:ffff:ffff is reserved for documentation use
- fc00:: to fdff:ffff:ffff:ffff:ffff:ffff:ffff:ffff are addresses reserved for internal network use and are not routable on the internet.