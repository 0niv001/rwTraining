*Network Security Group*
- NSG allows for network traffic filtering to and from AZ resources in VN.
- NSG has rules defining how traffic is filtered
- Can associate only one NSG to each VN subnet and interface in VM, but as many subnets and interfaces.

**Difference between NSG and Firewall
- Firewalls complements NSG, by providing defence in depth.
- NSG provide filtering to limit traffic to resources within the VN in a subscription, whilst Firewall provides network and application level protection across subs and networks.