- Can take O(n) time in the worst case, the average is O(1), depends on how well hash functions distributes set of keys
- Fast dictionary operations with O(1) time
- EV- Not suited for sorting items since data is scattered in memory
- Apps need dynamic set that only supports insert, search and delete operations
- Use a lot less storage than direct address tables.

Direct address tables:

- Technique that works best with small number of keys
- We assume that no two elements have the same key.
- EV- only good when there aren’t many keys

Hash function

- Can be used to compute slots from the key
- Tries to satisfy assumption of simple uniform hashing
- Can’t check because of probability of distribution

Division Method

- Computes hash values as the remainder when key is divided by prime number
- We map a key k, into one of m slots by taking the rest of k/m→ h(k) = k%m
- Tends to be quite fast,
- We avoid values of n, should not be a power of 2, a prime not too close to it, is a good choice.

Multiplication Method

- First we multiply the key k by a constant A in the range 0 < A < 1 and extract the fractional part of kA. Then we multiply the value by m and take the floors of the result.
- The hash function is h(k) = [m(kA %1)]
- One advantage is that the value of m is not critical.
- Typically chosen to be a power of 2 since we can easily implement the function on most computers.

Collision

- When two or more keys hash into the same slot (Array index)
- If set of keys is ≤ than has table then it won’t occur
- One way to reduce collision is to make H appear to be random.
- How to deal with collision:
    
    Chaining- Preferred method
    
    - Easier to implement
    - Less sensitive to hash functions
    - Hash table never becomes full, as added keys are in separate linked list
    - Takes more space in case of collision
    - Difficult to serialise data from hash table
    - Cache performance not good as keys are stored in linked list
    
    Open Addressing
    
    - All keys are stored in has table itself, each entry have a dynamic set || nil
    - we examine slots until we find the element or we realise it’s not in the table.
    - We can store linked list for chaining inside the hash table in the unused hash table slots.
    - Examining a slot is known as probe:
        - Linear
        - Quadratic
        - Double Hashing
    - Instead of following pointers we compute the sequence of slots to be examined, allowing for extra memory, less collisions and quicker retrieval.
    - EV
        - Better cache performance
        - Easier to serialise data
        - Avoids pointers altogether
        - Hash table may become full
        - Requires more computation
        - Needs extra care to avoid clustering