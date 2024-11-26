---
aliases: []
---
*Domain name server*
Translation of [[IP]] addresses into website names, and vice versa. 

Services offered on top of translating [[IP]] addresses:
- Host aliasing: easier to remember names for web pages
- Load distribution: busy sites are replicated over many different servers, with different IP addresses.

DNS uses servers organised in a hierarchy based on domain levels:
Root DNS ⇒Top Level Domain ⇒ Authoritative DNS server

Caching reduces delays by saving a list of IPs of visited pages to reduce amount of requests.