Responsible for [[Ethernet]] and [[MAC]] addressing, prepares the data for transmission on LAN. 

Datalink layer is made up of 2 sublayers
1. MAC
2. LLC

Devices include [[Switches]] , network adapters and bridges. 
### Error detection and correction
**Types:
1. Single bit errors: Only one bit of data is changed, least likely error. 
2. Burst error: 2+ bits in data have changed, likely in serial transmissions. 

**Techniques 
1. Simple parity check
	- Identifies errors in async transmissions and byte oriented protocols. 
	- An extra bit -parity- is appended so the number of 1s becomes even
1. 2D parity check
2. Checksum
	- Data is divided in segments
	- All segments are added and the sum is complemented, if the result is 0 the data is accepted. 
1. Cyclic redundancy check