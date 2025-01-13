
## Arrays
- Store multiple values in the same variable.
- Fixed in length. 
```java
String[] cars = {"Ferrari", "RedBull", "McLaren"};

String[] cars = new String[3]; //Create array with empty spaces

String[][] nested = {{ }
					 { }}

Object[] name = new Object[3]; // Create array of objects
name[index] = object; // add object to array

```
### List implementation
**Array list**
- Store and manipulate dynamic collection. 
- Have to use reference data types. 

```java
ArrayList<Integer> arrList = new ArrayList<>();

arrList.add(3);

arrList.remove(index);

arrList.get(index);

arrList.set(index, element);
```

**Stack**
- Subclass of vector - LIFO (Last in, First out)
- Quick access to last item. 
- Thread safe and simple to use, can dynamically be sized. 
- EV - Legacy class, use of it is discouraged. 
```java
Stack<Integer> stack = new Stack<>();

stack.push(1); //Add item to stack

stack.pop(2); //Remove and return first item in stack

stack.peek() //Return item at top of stack without removing it

stack.empty() // Empties out the stack 
```

**Linked List**
- *Components:*
	- Header: Pointer to first linked element
	- Size: Number of elements in LinkedList
	- modCount: Modifications made to LinkedList
- Part of collections framework, implements Deque interface.
- Based on doubly linked list - Allows for bidirectional transversal. 
- Much faster and efficient than ArrayList when adding, unless adding to end. 
- When searching you need to iterate through each one. 
- Good for dataset with less updating. 
- Dynamic sizing. 

```java
LinkedList<Integer> linkedList = new LinkedList<>();

linkedList.addFirst();
linkedList.addLast();
linkedList.removeFirst();
linkedList.removeLast();
linkedList.contains(Object);
linkedList.size();
```

### Set implementation
**Hash Set**
- Use [[Hash Tables]] to store unique elements. 
- Hash function maps keys to associated values. 
- O(1) Time complexity by converting the key into an index in the array. 
- Does not keep order
- Allows null elements
- Requires more memory

```java
HashSet<Integer> hashSet = new HashSet<>();

hashSet.add();
hashSet.remove(); // Returns true if an element was removed 
hashSet.contains();
hashSet.size();
hashSet.isEmpty();

```

**Linked Hash Set**
- Combination of Hash Set and doubly linked list. 
- Keeps order and is unique but takes up a lot of memory. 
- Does not have any sorting. 
- Ideal for collections of unique elements with predictable iteration order. 

```java
LinkedHashSet<String> lhs = new LinkedHashSet<>();

lhs.add();
lhs.remove();
lhs.iterator(); // Retunrs iterator over the elements of set in insertion order. 

```

**Tree Set**
- Implemented using a tree map, guarantees elements are sorted in ascending order, according to natural ordering, or by comparator provided at the start. 
- Easy to iterate over elements in specific sequence
- No null elements
- Very slow compared to HashSet and takes up a lot more memory due to tree structure. 

```java
TreeSet<Integer> treeSet = new TreeSet<>();

treeSet.add();
treeSet.remove();
treeSet.first(); //Returns first / lowest element in the set
treeSet.descendingSet(); // Returns reverse order view of elements in the set

```
### Queue Implementation
**Priority Q**
- Process elements based on priorities. 
- Use heap based data structure to order elements. 
- Priority determined by natural ordering of elements or by comparator. 
- Elements with highest priority are always at the head of the Q. 
- Does not allow null elements. 
- NO random access, can only access head of Q. 

```java
PriorityQueue<Integer> pq = new PriorityQueue<>();

pq.offer(element); // insert element in PQ, return true if successful
pq.peek(); // retrieves but doesn't remove head of Q, null if empty
pq.poll(); // retrieves and removes head of Q, null if empty 
```

**Array Deque**
- Resizable array implementing deque interface. 
- Can be both FIFO and LIFO - Versatile for many different applications. 
- Can have any object types inside of it.  
- No capacity restrictions, and Efficient for additions and removals > LinkedList
- Uses a lot of memory because of resizing, especially if done frequently. 

```java
ArrayDeque<String> dq = new ArrayDeque<>();

dq.addFirst();
dq.addLast();
dq.pollFirst();
dq.pollLast();
dq.peekFirst();
dq.peekLast();
```

### Maps
Collection that maps keys to values, where keys have to be UNIQUE, each key can map at most one value. 

Relationships established between keys and values allow for efficient retrieval and manipulation of data. 

**Hash Map**
- Constant time performance for basic operations. 
- Does not guarantee order of elements over time. 
- Constructed with initial capacity (N of buckets ) and load factor (how full table can get before capacity is automatically increased) - Usually doubling the amount of buckets. 
- Can have null values and keys. 

```java

hm.put(K,V)
hm.get()
hm.remove()
```

**Enum**
- Used with Enum keys. 
- Efficient (Time + space) and type safe way to implement enum constants to values. 
- Keys are kept in natural order. 
- Does not allow for null keys. 

```Java
import java.util.EnumMap;
enum Day {MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY, SUNDAY}

EnumMap schedule = new EnumMap<>(Day.class);

schedule.put(Day.MONDAY, "Value");
schedule.get(SUNDAY); // return value for specified key, or null. 
schedule.containsKey(MONDAY); // 1 if map contains mapping for the key
schedule.keySet(); // return set view of keys
schedule.entrySet(); // view of the mappings in the map 
```

**Tree**
- Uses Red-Black tree structure.
- Stores KV paris in sorted order. 
- Can use [[Binary Search]]
- Remove values by keys. 
- Slower than HashMap and requires more. 

```java

```

*Iterator*
- Interface for collection transversal, more powerful than for each loop. 
- Allows for removal of elements from collection during iteration. 
```Java
Iterator iter = collectionName.iterator();

while(iter.hasNext()){
	Integer nums = iter.next();
	sout(nums)
}
```
