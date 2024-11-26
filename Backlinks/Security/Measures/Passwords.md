Mostly text based [[Authentication]]

Passwords are stored using [[Hashing]] methods to make a representation of them, the hash is compared to the stored value.

Network snooping ( packet sniffing ) is quite easy to do, anything sent over the internet can be looked at and stored. If we send passwords over the internet someone could take it. If we send hashes across the network, you only need to take the hash to authenticate.

Because most logins happen via the internet or network, we need to establish where should the [[Authentication]] process take place.

Can get very close to securing networks against replay attacks, by using encrypted connections.

**Password Issues** 
- Sharing usernames and passwords. 
- Writing them down. 
- Using easily guessed / reusing passwords. 
- Shoulder surfing. 

**Attacks on passwords**
- Brute force: Generate passwords and compares results with values
- Dictionary: Rely on words hashing each one, 50% success against most DBs
- Rainbow tables: Fastest method, DB of strings and hashes, which are compared against compromised file. 
- Key loggers: Store what users type and relay it to attackers
- [[Social Engineering]]


**Protecting against password attacks**
- 2FA
- Password rules e.g. Length and characters, increasing complexity
- Limit number of failed log in attempts e.g. lock out timing. 
- Good practice to record failed attempt to identify attacks. 
- Remove passwords from main user files and store in shadow file. 
	- Doesn't stop brute force and bulk guessing. 