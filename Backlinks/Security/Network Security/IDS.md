*Intrusion detection systems* -  form of monitoring looking at real time events to find abnormalities. 

Allows for automated inspection of logs and real time systems to detect intrusions and system failures. 

Can recognise attacks from external connections, and attacks spread internally like worms, once detected they raise alarms, allowing for timely and accurate response. 

These refer to capabilities that are part of isolating and protecting a more secure domain from a less secure one. 

Can be classified as host based (HIDS), which monitors a single computer/host, or a network based (NIDS) which looks at network traffic patterns. 

**HIDS**
- Looks at activity on a single computer e.g. process calls and host based [[Firewall]] logs.
- Can examine in more detail than NIDS, and can pinpoint compromised files and processes used by hackers.
- Can detect anomalies that NIDS can't e.g. infections where systems are controlled remotely.
- HIDS are more costly to manage as they need admin attention on each system, whilst NIDS support centralised admin.
- HIDS cannot detect attacks on other systems. 

**NIDS**
- Monitors and evaluates network activity to detect attacks or event anomalies. 
- Can’t look at encrypted traffic but can look at other packet details. 
- Can monitor large networks using remote sensors to collect data at key network points, and places that support port mirroring and other network taps. 
- Little negative effect on the network performance, or other computers. 
- Can detect start of an attack but can’t determine their success e.g. if systems, files or apps were infected. 

**Security Information and Event Management (SIEM)**
- Gather log data from different sources to asses and address security concerns. 
- Logs can be used along other security implementations as part of a security program. 