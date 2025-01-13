Designing architecture, components and interfaces for a system so it meets requirements

Ensure system can withstand real world conditions - reliable, scalable, easy to maintain as applications grow. 

Good system design makes it easy to see how all parts of the system are connected, interact and function together. 

However process can be time consuming, especially for large and complex systems. 

Part of [[SDLC]], without design you cannot do the implementation or testing part. 

Represents the business logic of the software, if design is not good it doesn't matter how well the code is written. 

Main objectives:
- Practicality
- Accuracy
- Completeness
- Efficiency
- Reliability
- Optimisation
- Scalability
## Components
Elements involved in design of system 
*Load balancers*
- Requests are divided across different servers. 
- Prevents overloading them. 
- Layer 4 / 7 - [[OSI Model]] Network layer, allocate requests according to port and destination IP / Distribute layers according to content - application layer. 
- Applications - Work with specific type of application or protocol E.g HTTPs

*Caching*
- Store frequently requested data, speeding up retrieval, enhancing performance and efficiency - Faster data and response time, Process more requests, Quick access
- Store a copy of frequently requested data in temporary storage 
	- Browser - Local cache. 
	- Server - no need for expensive DB queries. 
	- DB cache query results for faster querying 

*CDN*
- Content Delivery Network
- Servers in different regions for faster delivery speed to users. 
- Pull and push based. 

Web Sockets allow for 2 way communication, whilst client server waits for client to make a request and then the server responds. 

**Partition tolerance** means the system will continue to operate despite network or node failures.
## Scalability
- Accommodate growing demand without compromising performance. 
- Ensures availability when there are spikes in traffic, Increases performance. 
- Think of concurrent users. 
- Vertical scaling - 
	- Increase capacity of single hardware e.g. add RAM or processor, 
	- requires no changes to application code, less complicated maintenance. 
	- Law of diminishing returns. 
	- Limited scalability, you can only add so much RAM. 
- Horizontal scaling
	- Adding more machines or servers, less downtime. 
	- More capacity, performance and better fault tolerance. 
	- Increases complexity, requiring robust infrastructure and management tools. 
- Factors affecting scalability
	- Performance bottlenecks - performance in lower than expected, DB & network. 
	- Resource utilisation:
	- Network latency:
	- Data storage and access:
- Challenges
	- Cost - increasing resources also increases costs. 
	- Complexity - As systems grow they become more complex making them more difficult to maintain and debug.
	- Data storage and access. 
	- Network latency. 
- Components
	- CDN. 
	- Caching. 
	- Load Balancers. 

## Availability
- Time system or service is accessible for user. Key for reliable and resilient systems. 
- Important for [[IR, BC, DR]], Compliance and UX. 
- How to achieve it:
	- Load balancers: Requests are divided between different servers.
	- Redundancies: If there is a failure another server can take over with no problems.
	- Monitoring and alerting: Identify problems instantly and alert admins 
	- Scalability: Scale easily, by adding more resources when needed. 

## Reliability
- Consistent performance and minimal failure
- High if repeatedly performs functions with success under certain conditions. 
- Factors affecting it 
	- Design and hardware quality
	- Bugs
	- Maint
- How to achieve it
	- Scalability
	- Load Balancing 
	- Monitoring
	- Redundancy
	- Fault tolerance 

## Design Interview
1. Understand problem and establish design scope
	- Ask as many questions to understand problem. 
	- Clarify requirements: Features, who the users are. 
	- Priority order of these features. 
	- Get order of magnitude right. 
	- Chase Bank - Low latency, high availability, scalability, reliability
2. Propose high level design
	- Load balancers / API Gateway
	- Persistance - Data storage layer
1. Design deep dive
2. Wrap up 

primary concerns
bandwidth 
Way to query the data needed, define API endpoints. 
Testing is very important. 
## Network Design
**Physical Design**
- [[Star topology]] allowing for easy troubleshooting and scalability, however this leads to a single point of failure. BUT other topologies have the same drawback. 
- Physical network isolation - using different hardware to separate parts of the network, e.g. using different switches to control access. 
- Switches distinguish the different devices connected to them so they route traffic to the specific device rather than all the devices, making traffic delivery more efficient and reducing congestion. 
- Ensure wireless access point was positioned in such a way that it ensured all the traffic went to the firewall first, ensuring security from potential threats. 

**Logical Design**
- [[Firewall]]Monitor and control incoming and outgoing traffic, block unauthorised access. Rules need to be well configured. 
- [[Switches]]for servers
- Logical segmentation and reduce costs as opposed to physical segmentation, less hardware needs to be purchased. 
- [[DMZ]]for network accessible by outside visitors, stays isolated from private network. 

*Routing and addressing*
- [[IPv4]] allows to create private address groups. 

**Availability**
- Access to resources is only available to those who have [[Authentication]]access 
- [[Access Control]] - Availability and security. Difficult to configure and manage on larger networks. 
- [[NAC]] to automate access control process. 
- [[Switches]]
- [[VLAN]]for [[Segmentation]]Devices with the same VLAN can communicate, but we also limit traffic. Configured for each department, limiting access to other departments.  
- Storage backups on and off site. 

**Scalability**
- [[DHCP]] Reduce likelihood of [[IP]]address conflicts on network. 
- [[NAT]]Give several private ip a single public one for accessing the internet, reducing number of public addresses.  Use [[Router]]and [[Firewall]]
- Systems already being used, making things easier for us to set up. 
- Reserve address ranges for future use. 
- [[STP]]

**Security**
- [[DoS]]
	- Load balancers spreading workloads across servers to prevent overloading them, help eliminate single point of failure and reduce attack surface. 
	- [[Firewall]] to filter [[IP]] making too many requests. 
	- [[Defence in Depth]]
- MITM - Intercept comms and data between devices on network. 
	- [[Authentication]]
	- [[Encryption]]
- [[Malware]]and [[Ransomware]]
	- [[Firewall]]
	- [[Antivirus]]
	- [[Authentication]]
	- [[Encryption]]
	- Monitoring [[IDS]][[IPS]]

**BYOD**
- Use personal devices in the workplace. 
- Difficult to enforce security policies. 
- Personal devices could have malware on them. 
- Data protection issues
- Chase bank app - Ensure it is not Jailbroken. 
- Client to site[[VPN]], creating a secure communication tunnel to allow access to corporate network. 


L1/L2/L3 Cache 

WebSocket - Allows for bi - directional communication. 


API Patterns
- REST - Stateless, 
- GraphQL - Make a single Query and choose what data you need,
- GRPC - framework, S2S Comms, uses protocol buffers. 


