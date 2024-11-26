Takes input set of data and returns a fixed length result -> *hash value.* 

Same input will produce the same hash, which can be used to identify the data.

Mostly used to store passwords - but hashes can be figured out, so passes are often salted, meaning that random values are often added to create unique hashes for the same input. If someone was to change the content of the input the hash will not match

These need to be nonreversible, unique and deterministic. 

Integrity protection is ensured by using a message digest or hash algo to produce a message [[Authentication]] code that is appended to the data before the encryption.

The most used methods used are MD6 and SHA-2, SHA-3