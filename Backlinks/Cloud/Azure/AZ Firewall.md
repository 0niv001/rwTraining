Cloud based network security service that protects the Azure virtual network resources.

Can be deployed to any VN, but best to set it on centralised VN, so that all traffic is routed through it.

Allows for control of traffic on all VNets across subs, as well as scaling for network traffic.

*Key features:
- High availability and availability zones: Nothing to configure, can span multiple availability zones.
- Network and app level filtering: Use [[IP]] address, port, and protocol to support domain name filtering HTTPs.
- Outbound SNAT, inbound DNAT to comm with internet resources: Translate private IP of resources to public to identify and allow traffic from VN to different destination, and vice versa.
- Multiple public IPs
- Threat intelligence: allows firewall to alert and deny traffic from malicious IPs and domains.
- Integrated with Azure Monitor: Can look at and analyse firewall logs.